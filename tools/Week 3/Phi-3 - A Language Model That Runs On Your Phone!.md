![Phi-3](https://media.licdn.com/dms/image/D4D12AQE-07X1ijhiFg/article-cover_image-shrink_600_2000/0/1716483690066?e=2147483647&v=beta&t=BCGKUC2qkoFhLOJQ8pFNZvSBjW0ELbrNYj0vRn14kyE)
<div align="center" ><i>Source : linkedin.com</i></div>


# Author

Tarun Krishnan (**ORCID**: [0009-0006-6647-127X](https://orcid.org/0009-0006-6647-127X))

# Introduction

In recent times, the battle for developing the most capable language model has intensified, with many big tech companies getting deeply involved in generative AI. This has led to the creation of massive models, some boasting even trillions of parameters. There is a common misconception that 'bigger is better,' meaning that people often think that the more parameters a model has or the more training data it is fed, the better it will perform. Enter Microsoft with their latest generative AI model, 'Phi-3', which has demonstrated better performance on standard open-source benchmarks (that measure the model’s reasoning ability) like MMLU and MT-bench than popular competitors Mixtral 8x7B and GPT-3.5, both of which contain billions more parameters than Phi-3. With Phi-3, one can now use a highly capable generative AI model on their phone to help with everyday tasks without concern for privacy, as the model can be downloaded on their handheld device and used without an internet connection, all for around only 2GB of storage space!

![Phi-3 on phones!](https://favtutor.com/articles/wp-content/uploads/2024/04/Microsoft-Phi-3-LLM-for-Phones.jpg)
<div align="center" ><i>Source : favtutor.com</i></div>

# Exploring Phi-3

Before we delve into what makes Phi-3 so special, let's briefly discuss the four variants of Phi-3:

- **Phi-3-mini**: This model has 3.8 billion parameters. It is designed for applications that need to run locally on a device, where tasks don't require extensive reasoning or where quick responses are necessary. This model was tested on an iPhone 14 with an A16 Bionic chip in fully offline mode and achieved more than 12 tokens per second!
- **Phi-3-vision**: A 4.2 billion parameter model based on Phi-3-mini, which possesses strong reasoning capabilities for image and text prompts.
- **Phi-3-small**: This version contains 7 billion parameters. It strikes a balance between performance and computational efficiency, making it suitable for tasks that need more capacity than the mini version but still benefit from a compact model size.
- **Phi-3-medium**: This is the largest in the Phi-3 family, with 14 billion parameters. It is more suited for complex tasks that involve advanced reasoning, data analysis, and understanding of context.

![Benchmark phi](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/benchmark-phi-tarun.png)
<div align="center" ><i>Comparison of Phi-3 Models and Its Competitors on Benchmark Tests</i></div>


Now that we know a bit about the different versions that Phi-3 has to offer, let's focus our attention on the Phi-3-mini.

## What Makes the Phi-3-mini so Powerful?

Although the name has 'mini' in it, its capabilities are anything but 'mini' and are immense compared to its competitors while having fewer parameters.
### Training Data

As with any AI model, the better the data, the better the performance. It is with this ideology that Microsoft decided to focus heavily on the type of data used to train the mini model. Recent trends show that companies tend to use more data and more computing resources to try to develop a 'smarter' generative model, but Microsoft went against this thought and limited the size of their training data, utilizing 'heavily filtered publicly available web data from various open internet sources' and 'synthetic LLM-generated data.' What is "synthetic LLM-generated data"? In simple terms, it means using a bigger, more powerful LLM to train a smaller LLM. Microsoft struck a gold mine with this combination, allowing the Phi models to pack a serious punch with fewer parameters and generate human-like text. The larger Phi-3 models, like Phi-3-small and Phi-3-medium, were trained using the same high-quality data but for much longer periods, thereby improving their individual performances on benchmark tests.
### Structure

Another strong suit of the mini is that it was built upon a similar block structure as Llama-2 and uses the same tokenizer with a vocabulary size of 320,641. This means that any software packages, tools, or libraries developed for Llama-2 can be directly adapted for use with Phi-3-mini without significant changes, thereby benefiting the open-source community.
### Context

The Phi-3-mini is built using a Transformer-Decoder, which is used in many modern language models and has a default context length of 4k. This implies that although it is small in size, it can accept large amounts of data to process and generate responses.
### Safety

Although generative models have improved in "conversing" with humans, at the end of the day, a generative model generates text based on predicting the next possible word/token and doesn't really understand human emotions. Due to this, there have been cases where models have produced content that has led to unfortunate circumstances for some of its users. Microsoft combats this issue through 'safety alignment in post-training, red-teaming, automated testing and evaluations across dozens of RAI harm categories' and by developing the mini model in 'accordance with Microsoft’s responsible AI principles.' These guardrails ensure a 'significant decrease in harmful response rates' and ensure the safety of users while using Phi models.
### Privacy

As mentioned before, having the model available to use on one's personal device allows users to be less concerned about their data being stolen or used for future model training purposes. Unlike other competitors, all requests by the user are processed locally, allowing not only faster turnaround response times but also eliminating the need for data to be sent to the cloud, which has its own potential safety issues.

## Drawbacks of Phi-3-mini

As with any development, all is not "sunshine and rainbows" and there are bound to be certain weaknesses in new inventions.
### Poor Performance on Factual Tasks

While Phi-3-mini achieves a similar level of language understanding and reasoning ability as some of the competitors in the field, it is still limited in its capacity to perform certain tasks. For instance, when working on tasks requiring a lot of 'factual knowledge,' it doesn't seem to perform well. This can further be observed in its low performance scores on the TriviaQA benchmark test. Microsoft, however, believes that such a drawback can be averted by connecting the mini model to a search engine. So if a user wishes to use the model to answer factual-based questions, they can connect to the internet and use an augmented version of the mini model.
### Language Restrictions

Another restriction with the mini model is that currently its working is mostly restricted to the English language. Steps are being taken by Microsoft to include 'more multilingual data' into their training data for their Phi-3-small model, and they have observed some promising signs through their experimentations. In the near future, we could definitely see the mini model possessing multilingual capabilities as well.
### Hallucinations

As with any language model, hallucinations are a challenge that Microsoft is trying to address. Hallucination can be thought of as the generation of inaccurate text due to the model not being prepared to answer a certain prompt posed by a user. With the use of highly curated data, Microsoft has been able to mitigate these issues to a certain extent, but further improvements are being done to the data and model to minimize these issues further.

# Quick and Easy Phi-3 Installation

Now that we have learned about how powerful Phi-3 can be, let's look at how you can easily start using this model!
## Step 1: Install Ollama

Ollama can be thought of as a platform that helps you easily download and access open-source language models. You can click on this link to reach the download page of Ollama: [Ollama Download Page](https://ollama.com/download). Ollama can be downloaded on macOS, Linux, and Windows.
## Step 2: Installing Phi-3

Once you have installed Ollama, open your command prompt/terminal and execute the following command:

```bash
ollama run phi3:mini
```

This will install the mini model that has 3.8 billion parameters. As of the time of this article, you can also install the medium model (which has 14 billion parameters) using the following command:

```bash
ollama run phi3:medium
```

![phi install](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/ollama-install-tarun.png)
<div align="center" ><i>Phi-3 Installation Process</i></div>

## Step 3: Trying Out Microsoft's Newest Innovation!

I have installed the mini version on my system, but feel free to try running the medium model. Once you download the model, you should see the following prompt:

![phi start](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/start-ollama-tarun.png)
<div align="center" ><i>Phi-3 Message Request</i></div>


If not, you can always run the same command that you ran to install your Phi-3 model.

![phi sample conversation](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/convo-phi-tarun.png)
<div align="center" ><i>Phi-3 Sample Conversation</i></div>

# Conclusion

The Phi-3 model series from Microsoft highlights the potential of high-quality, efficient AI models that don't rely on sheer size to achieve outstanding performance. With variants like Phi-3-mini offering powerful local processing capabilities and larger models providing advanced reasoning, Phi-3 caters to a broad spectrum of needs. Microsoft's innovative approach to training data and model structure, combined with a strong emphasis on safety and privacy, sets a new standard in the field of generative AI. The future of generative AI looks promising with the continued development and refinement of models like Phi-3.


# References 

1) AI Revolution. “Microsoft’s New PHI-3 AI Turns Your IPhone into an AI Superpower! (Game Changer!).” _YouTube_, 23 Apr. 2024, www.youtube.com/watch?v=F-FL2f9rRxQ. Accessed 5 Aug. 2024.

2) Matthew Berman. “Phi-3 BEATS Mixtral and Fits on Your Phone!” _YouTube_, 24 Apr. 2024, www.youtube.com/watch?v=Enp70Kkjb8k. Accessed 6 Aug. 2024.

3) Abdin, M., Jacobs, S. A., Awan, A. A., Aneja, J., Awadallah, A., Awadalla, H., Bach, N., Bahree, A., Bakhtiari, A., Bao, J., Behl, H., Benhaim, A., Bilenko, M., Bjorck, J., Bubeck, S., Cai, Q., Cai, M., Mendes, C. C., Chen, W., . . . Zhou, X. (2024). Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone. _ArXiv_. /abs/2404.14219