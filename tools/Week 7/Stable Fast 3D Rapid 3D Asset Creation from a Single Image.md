# Stable Fast 3D: Rapid 3D Asset Creation from a Single Image

Discover the Power of Stable Fast 3D

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-1.png)
<div align="center"><small>Created using DALLE on September 19, 2024, using prompt "2D-to-3D transformation"</small></div>

## Authors

- [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)<br>
## Introduction

In today's rapidly growing digital industries—such as gaming, virtual reality, and design—efficient and high-quality 3D asset creation is becoming increasingly critical. Traditional methods for generating 3D models are often time-consuming and computationally expensive, making them impractical for many real-time applications.

**Stable Fast 3D (SF3D)** is a cutting-edge 3D asset generation tool designed to solve this problem. This model can transform a single image into a fully textured, UV-unwrapped 3D model in just **0.5 seconds**. Built on the foundation of advanced techniques in mesh generation, SF3D is equipped with fast UV unwrapping and material learning, ensuring high-quality textures and realistic material properties.

The key advantage of SF3D lies in its speed and ease of use. It removes the need for complex manual processes, making it ideal for professionals in fields like gaming, retail, architecture, and design, who need to quickly generate detailed 3D assets. Furthermore, the model incorporates a delighting process, enabling the assets to adapt to various lighting conditions, adding versatility to its applications.

With SF3D, users can efficiently create 3D assets without sacrificing quality, significantly streamlining workflows and accelerating creative projects.

## The Mechanism and Performance of Stable Fast 3D

This diagram below provides an overview of the **Stable Fast 3D** model's architecture. It begins with an input image, which is processed into **Triplane Tokens** through an enhanced **Transformer**. The **Material Net** estimates surface properties like metallicity and roughness, while the **Light Net** handles illumination effects. The **DMTet** module extracts the 3D mesh, calculating density, offsets, and normals. Finally, the model applies a fast **UV-unwrapping** technique to produce a textured 3D model. This architecture allows for quick, high-quality 3D asset generation from 2D images.


![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-14.jpg)
<div align="center"><small>The Mechanism of Stable Fast 3D, downloaded from Stability.AI website</small></div>

The second chart provides a **quantitative comparison** of **Stable Fast 3D** against other leading 3D reconstruction models. The **x-axis** represents the inference time (seconds per image), while the **y-axis** indicates the **F-Score**, which measures accuracy. As demonstrated by the green star in the chart, **SF3D** achieves the **highest F-Score** with the **shortest inference time**, outpacing models like **TripoSR**, **OpenLRM**, and **InstantMesh** in both speed and quality of reconstruction.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-15.jpg)
<div align="center"><small>The performance of Stable Fast 3D, downloaded from Stability.AI website</small></div>

## How to use Stable Fast 3D

There are generally three ways to use Stable Fast 3D, which I will introduce in the following sections.

### Method 1: Using Hugging Face

Stable Fast 3D model code is available on [Github](https://github.com/Stability-AI/stable-fast-3d) and [model weights](https://huggingface.co/stabilityai/stable-fast-3d) and [demo space](https://huggingface.co/spaces/stabilityai/stable-fast-3d) on Hugging Face. To try the model, you can simply use the demo space on Hugging Face.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-2.png)
<div align="center"><small>Demo space of Stable Fast 3D on Hugging Face</small></div>

As shown in the image, you can upload your own 2D picture, and the model will generate a corresponding 3D model based on it. For example, I uploaded a picture of Mole Warrior, and the model produced a high-quality 3D representation of the character. The results were impressive, with detailed rendering on all sides of the model. If your 2D image contains a background, you can use the "Preview Background Removal" option provided by the model to automatically crop it out.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-3.png)<div align="center"><small>Mole warrior picture as an example</small></div>

After clicking "Run," you’ll receive a high-quality 3D model of Mole Warrior. As shown, the model includes intricate details, with the back and sides of the character completed seamlessly.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-4.gif)
<div align="center"><small>Mole warrior 3D model created by Stable Fast 3D</small></div>

### Method 2: Using Stable Assistant

In addition to using Hugging Face, you can also access **Stable Fast 3D** through **Stable Assistant**. Stable Assistant is a user-friendly chatbot developed by Stability AI, featuring the latest advancements in text and image generation technology, such as **Stable Image Ultra**, **Stable Video**, **Stable Audio**, **Stable Image Services**, and **Stable LM 2 12B**. However, in this article, we focus specifically on its **Stable Fast 3D** function, which enables 2D-to-3D conversion, as that is the subject of our discussion.

#### Step 1: Sign Up or Sign In to Your Account

Go to the [Stable Assistant](https://stability.ai/stable-assistant) official website to sign up or log in to your Stability.ai account. While Stable Assistant is a paid service, you can take advantage of a free 3-day trial to explore its features.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-5.jpg)
<div align="center"><small>Stable Assistant official website</small></div>

#### Step 2: Upload an Image to Create Your Model

After setting up your free trial, you can upload an image to the chatbox and request it to generate a 3D mesh.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-6.jpg)
<div align="center"><small>Get started to use this Chatbox</small></div>

For example, we used a robot image, and here is the resulting 3D mesh model.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-7.jpg)
<div align="center"><small>The picture of a robot</small></div>

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-8.gif)
<div align="center"><small>3D robot mesh generated by Stable Fast 3D, downloaded on Unsplash</small></div>

In addition to uploading images, we can also use prompts to create the models we need. For example, I used the prompt “Make a 3D model of a horse” to generate a new mesh, and here is the result.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-9.jpg)
<div align="center"><small>Using only prompt to generate 3D mesh</small></div>

The generated 3D model is impressive, with remarkable attention to detail and smooth, well-defined surfaces. The textures are accurately rendered, and the overall structure of the mesh feels natural and cohesive. The model showcases excellent depth and realism, making it suitable for a wide range of applications, from gaming to virtual reality. The quality of the generated mesh highlights the capability of Stable Fast 3D in producing high-quality assets quickly and efficiently.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-10.gif)
<div align="center"><small>3D horse mesh generated by Stable Fast 3D</small></div>

### Method 3: Intergrate Stable Fast 3D into Your Application

Of course, we can also integrate the functionality of Stable Fast 3D into our own applications by using Stability's API key. This allows us to implement 2D image-to-3D model conversion directly within our software. The Stability API key is a paid service, but new users receive 25 free credits upon account creation. Each successful use of the Stable Fast 3D feature consumes 2 credits.

#### Step 1: Get Your Stability API Key

First, visit the Stability.ai website and sign in to obtain your API key. Simply click on **Create API Key**, and you're all set to go.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-11.jpg)
<div align="center"><small>Get your API keys</small></div>

#### Step 2: Build a Demo

Next, we’ll implement our code logic. Below is a simple demo that demonstrates how to use an API key to access and utilize the **Stable Fast 3D** model, successfully achieving 2D image-to-3D model conversion. With this demo as a guide, you can easily integrate the code logic into your own software based on your specific needs.

Here's the code:

```
import os
import requests

# Set API key and file paths

API_KEY = "Your API key"  # Replace with your actual API key

base_path = r "Your file path"  # Replace with your actual path

image_file = os.path.join(base_path, "Your_image_name.png")  # Path to the image file

output_file = os.path.join(base_path, "Your_model_name.glb")  # Path to save the 3D model

# Send POST request to the API

response = requests.post(

    "https://api.stability.ai/v2beta/3d/stable-fast-3d",
    headers={
        "authorization": f"Bearer {API_KEY}",
    },
    files={
        "image": open(image_file, "rb")
    },
    data={
        "texture_resolution": 1024,  # Optional parameter: Choose 512, 1024, or 2048
        "foreground_ratio": 0.85     # Optional parameter: Adjust the foreground ratio
    },
)

# Handle the response and save the 3D model

if response.status_code == 200:
    # Save the generated GLB file to the specified path
    with open(output_file, 'wb') as file:
        file.write(response.content)
    print(f"3D model saved successfully as {output_file}")
else:
    # Handle errors
    print(f"Error: {response.status_code}")
    raise Exception(response.json())
```

#### Step 3: Get started to try this model

Here, we assume that our Python file is named **Demo**. You can run the following command in the terminal to execute the demo:

```
Python Demo.py
```

We used a cartoon character image as an example. Below is the original image along with the generated 3D model:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-12.png)
<div align="center"><small>The picture of a cartoon character</small></div>

The GLB model file we generated is supported by several software programs, such as Blender, Microsoft 3D Viewer, and Unity. Here, we introduce a free website called [**glTF Viewer**](https://gltf-viewer.donmccurdy.com/), where you can view the model we just created. Below is the model display:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/sf3D-13.gif)<div align="center"><small>3D cartoon mesh generated by this demo</small></div>

## Conclusion

**Stable Fast 3D** revolutionizes 3D asset generation by offering rapid, high-quality results from a single image in just 0.5 seconds. Its ability to produce UV-unwrapped, textured 3D models with advanced material learning and lighting flexibility makes it an essential tool for industries like gaming, virtual reality, and design. With its versatile use cases—whether through Hugging Face, Stable Assistant, or API integration—SF3D simplifies and accelerates workflows, ensuring professionals can generate detailed 3D models quickly and efficiently without compromising on quality.

## References

1) Stability.AI Team. “Introducing Stable Fast 3D: Rapid 3D Asset Generation From Single Images.” _Stability.AI Official Website_, 1 Aug. 2024. [Read me](https://stability.ai/news/introducing-stable-fast-3d). Accessed on 19 Sep 2024.
2) *Technical Support Documentation for Stable Fast 3D.* [Read me](https://platform.stability.ai/docs/api-reference#tag/3D). Accessed on 19 Sep 2024.