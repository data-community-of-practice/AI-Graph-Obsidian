# How to Run Llama 3.2 on Android Phone

Header image:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271921073.png)

Tags: AI, LLM, Llama3.2, Android

# How to Run Llama 3.2 on Android Phone

## A Step-by-Step Guide to Running Llama 3.2 and Other Large Models on Android Using Ollama

## Authors

- [Zijian Yang](https://www.linkedin.com/in/zijian-yang/) (**ORCID:** [0009-0006-8301-7634](https://orcid.org/0009-0006-8301-7634))

## Introduction

At the recently concluded Meta Developer Conference, Llama 3.2 made a dazzling debut. This time, not only does it boast **multimodal capabilities**, but it has also partnered with companies like Arm to launch a "mobile" version optimized specifically for Qualcomm and MediaTek hardware.

Specifically, Meta released four models of Llama 3.2:

- Multimodal versions with 11 billion and 90 billion parameters
- Lightweight pure-text models with 1 billion and 3 billion parameters

According to official data, Llama 3.2 11B and 90B have demonstrated **performance surpassing that of closed-source models** of similar size.

In particular, for image understanding tasks, Llama 3.2 11B outperformed Claude 3 Haiku, and the 90B version can even hold its own against GPT-4o-mini.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271909901.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271909444.png)

Currently, the two largest models of Llama 3.2, 11B and 90B, support image inference, including document-level chart understanding, image description, and visual localization tasks, such as pinpointing objects in images based on natural language descriptions.

For example, users can ask, "Which month had the best sales last year?" and Llama 3.2 can quickly provide an answer by reasoning over available charts.

The lightweight 1B and 3B versions are pure-text models but also boast multilingual text generation and tool-calling capabilities. Meta states that these models enable developers to build personalized, on-device general-purpose applications — these applications offer strong privacy since data doesn't need to leave the device.

Running these models locally has two main advantages:

- Prompts and responses can feel instantaneous because the processing is done locally.
- When running models locally, there's no need to upload private information like messages and calendars to the cloud, ensuring data privacy. Since processing is local, applications can determine which tasks can be handled on-device and which require the more powerful cloud-based models.

Although no products currently allow mobile devices to run these powerful lightweight models effectively, we can still use a Linux environment to get a preview with Ollama.

This article will guide you on installing Termux on an Android phone and compiling and installing Ollama in its Linux environment to run Llama 3.2 locally. The same method can be used to run any other supported models.

### Technical Background of Lightweight Models (Optional)

As Meta mentioned during the release of Llama 3.1, powerful teacher models can be leveraged to create smaller models with better performance. Meta pruned and distilled the 1B and 3B models, making them the first lightweight Llama models capable of efficient on-device operation.

Through pruning techniques, the Llama series models' size can be significantly reduced while retaining as much of the original knowledge and performance as possible. During the development of the 1B and 3B models, Meta employed a one-time structured pruning strategy derived from Llama 3.1's 8B model. Specifically, Meta systematically removed certain parts of the network and adjusted the weights and gradients accordingly, resulting in a smaller, more efficient model while ensuring it maintained the same performance level as the original network.

After completing the pruning step, Meta applied knowledge distillation to further enhance the model's performance.

Knowledge distillation is a technique where a larger network transfers knowledge to a smaller network. The core idea is that, guided by the teacher model, the smaller model can achieve better performance than if it were trained independently. In the 1B and 3B models of Llama 3.2, Meta introduced the outputs of Llama 3.1's 8B and 70B models during the pre-training phase as token-level targets for the training process.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271909190.png)

In the post-training phase, Meta employed a method similar to that used for Llama 3.1 — conducting multiple rounds of alignment on the pre-trained model. Each round included Supervised Fine-Tuning (SFT), Rejection Sampling (RS), and Direct Preference Optimization (DPO).

Specifically, Meta extended the context window length to 128K tokens while maintaining the same quality as the pre-trained model.

To enhance the model's performance, Meta also utilized synthetic data generation. They curated high-quality mixed data to optimize the model's abilities in summarization, rewriting, following instructions, semantic reasoning, and tool usage.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271909990.gif)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910909.gif)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910982.gif)

*The above demonstration is based on an unpublished quantized model.*

## Test Device

The phone I used is a Samsung S21 Ultra released four years ago, with the following specifications:

- Processor:
    - Model: Qualcomm Snapdragon 888
    - Process: 5nm
    - CPU architecture: 1+3+4 octa-core design
        - 1 Cortex-X1 prime core, clocked at 2.84 GHz
        - 3 Cortex-A78 performance cores, clocked at 2.4 GHz
        - 4 Cortex-A55 efficiency cores, clocked at 1.8 GHz
    - GPU: Adreno 660
- Memory:
    - RAM: 16GB LPDDR5
    - Storage: 512GB UFS 3.1 flash memory

Through testing, this device runs the Llama 3.2 3B model with slight lag but overall smoothly. Running the Llama 3.2 1B model is smooth without issues.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910301.png)

When generating answers with the model, my phone's 16GB of memory had only 2.8GB available, and the temperature noticeably increased. Please note, the method described in this article does not ensure the use of the GPU for inference, as the GPU on such mobile devices cannot be recognized.

Therefore, to run Llama 3.2 on an Android device, all you need is an Android phone, a network connection, and some patience.

Let's get started.

## Download and Install Termux

> Termux is a powerful terminal emulator and Linux environment app for Android, which provides a wide range of tools typically available on a full-fledged Linux system. What sets Termux apart from other terminal emulators is its ability to run without the need for root access, making it accessible to a broader audience of Android users. With Termux, you can install and run various programming languages, tools, and packages directly on your Android device, turning it into a portable development environment.
> 

You can download the latest version directly from Termux's GitHub page:

[https://github.com/termux/termux-app/releases](https://github.com/termux/termux-app/releases)

Here, we choose to download [`termux-app_v0.119.0-beta.1+apt-android-7-github-debug_arm64-v8a.apk`](https://github.com/termux/termux-app/releases/download/v0.119.0-beta.1/termux-app_v0.119.0-beta.1+apt-android-7-github-debug_arm64-v8a.apk).

Once the download is complete, install the APK file on your Android device.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910002.jpg)

## Environment Setup

After launching Termux, you will see an interface similar to a regular Linux terminal. You can open this article on your phone to easily copy the many commands that follow.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910449.png)

Next, we need to run the following command:

```bash
termux-setup-storage
```

> The `termux-setup-storage` command in Termux is used to grant the Termux app access to the shared storage on your Android device. This command creates a directory in the Termux home directory called `storage`, which contains symbolic links to various standard Android storage directories, such as `downloads`, `pictures`, `music`, and more. By running this command, you allow Termux to read from and write to your device’s external storage, making it easier to manage files, access media, and save or retrieve data between Termux and other apps.
> 

After running the command, a system permission prompt will appear. Click `Allow permission`, and then press the back button to continue.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910575.png)

Next, run the following command:

```bash
pkg upgrade
```

> The `pkg upgrade` command in Termux is used to update all installed packages to their latest available versions. It ensures that your system and applications are up-to-date, improving performance, security, and compatibility with other software.
> 

During the execution, you will need to input `Y` to continue updating the program.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910904.png)

Here, simply press `Enter` to proceed.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910418.png)

After the update is complete, we will begin installing the necessary packages for the environment:

```bash
pkg install git cmake golang
```

> The command installs three packages: Git (a version control system), CMake (a build system), and Go (the Go programming language), enabling you to manage source code, build software, and develop in Go.
> 

Once completed, it will display as shown in the image below.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271910935.png)

## Compile and Install Ollama

> **Ollama** is a platform designed to make it easier for developers to run large language models (LLMs) like LLaMA locally on their own machines. It provides a streamlined and optimized environment for managing, running, and interacting with these models, focusing on performance and accessibility. Ollama simplifies tasks like setting up dependencies, optimizing hardware usage (e.g., GPU acceleration), and providing pre-trained models ready for local execution.
> 

We will pull the code from Ollama's GitHub repository to our local machine:

```bash
git clone --depth 1 https://github.com/ollama/ollama.git
```

The results after execution.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271911783.png)

Next, navigate to the ollama folder and execute the Go code generation command:

```bash
cd ollama
```

```bash
go generate ./...
```

After a short wait, you will see.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271921637.png)

Next, compile the Go code in the current directory into an executable binary. This command takes all the Go source files in the directory and creates a compiled binary that can be run.

```bash
go build .
```

Then we start an Ollama server in the background:

```bash
./ollama serve &
```

> This command starts the Ollama server in the background (due to the `&`), allowing it to serve requests without blocking the terminal. The server will continue running and can be accessed for interactions with the model while the terminal is free for other commands.
> 

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271921113.png)

At this point, by running `ls`, we can see that `ollama` has been created as an executable file.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271922025.png)

## Running Llama 3.2

Ollama offers a variety of original and quantized models for Llama 3.2, including 1b and 3b versions. The default is 4-bit quantization. You can select a model from the following link:

[https://ollama.com/library/llama3.2:3b](https://ollama.com/library/llama3.2:3b)

Run the following command to download the Llama 3.2 3b quantized model:

```bash
./ollama run llama3.1:3b --verbose
```

> The `--verbose` flag is used to enable detailed logging during the execution of the model. It is optional and can be omitted if you don't need detailed logs.
> 

Please be patient during the download process.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271922838.png)

When you see the "Send a message" prompt appear, it's ready to use. It is worth noting that Llama 3.2 3B may still provide incorrect answers to logical questions such as "Which is larger, 9.11 or 9.9?".

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271922517.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202409271929476.png)

You can exit the chat terminal using `Ctrl+D`.

If you want to terminate the response process, press `Ctrl+C` to stop generating the response.

If you find the response speed too slow, you might try using the Llama 3.2 1B model, which will increase the response speed.

## Cleanup Tips

You may want to remove the 'go' folder that was just created in your home directory. If so here is how to do it.

```bash
chmod -R 700 ~/go
rm -r ~/go
```

Currently, termux does not have .local/bin in its PATH (though you can add it if you would prefer). If you would like to move the ollama binary to the bin folder you can do the following.

```bash
cp ollama/ollama /data/data/com.termux/files/usr/bin/
```

Now you can just run `ollama` in your terminal directly!

## **Conclusion**

In conclusion, the release of Llama 3.2 marks a significant milestone in AI technology, particularly in its ability to deliver high performance on mobile devices. With its multimodal capabilities and lightweight models, Llama 3.2 enables developers to create on-device applications that prioritize both privacy and responsiveness. 

This article demonstrates how to run the 1B and 3B versions of Llama 3.2 on Android devices, starting with the installation of Termux, followed by setting up the necessary environment, compiling Ollama, and finally running the model locally. The ability to process AI tasks directly on mobile hardware, even older models like the Samsung S21 Ultra, highlights the potential for real-world applications, offering a secure and efficient way to harness AI’s power without relying on cloud infrastructure. 

As we move forward, the ability to run these sophisticated models locally on mobile devices could revolutionize industries by making advanced AI more accessible, secure, and user-friendly.

## **Source**

- [https://gitlab.com/-/snippets/3682973](https://gitlab.com/-/snippets/3682973)