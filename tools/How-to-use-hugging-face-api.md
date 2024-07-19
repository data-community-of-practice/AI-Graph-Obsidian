# How to use Hugging Face API

Getting started to join Hugging Face community

![[thumbnail-image.png]](../img/images-wendi/thumbnail-image.png)
<div align="center"><small>All the models gathered on the Hugging Face Hub （created using DALLE on July 18, 2024）</small></div>


## Authors

- Wendi Fan (**ORCID: 0000-0003-0284-9166**)

## Introduction

The Hugging Face Hub is a collaborative open-source platform that hosts a vast array of models, datasets, and demos for the machine learning community. With its diverse range of accessible models, it caters to various daily work needs. This article will introduce how to use the Hugging Face API and utilize models from the platform in your own applications step by step.

## Hugging Face API Tutorial

To use models from the Hugging Face platform in a local application or service with Hugging Face API, users can perform complex natural language processing tasks without needing to delve into the details of model implementation or large-scale dataset training processes. Here, we will give an image-to-text model from Hugging Face Hub as an example to show you how to use it with Hugging Face API.

### Step 1: Get your API Token

To get Started, register or Login to your Hugging Face account first. Next, go to settings page and click **Access Tokens**. Next, click **Create new token**.

![[Step1.png]](../img/images-wendi/Step1.png)
<div align="center"><small>Hugging Face account settings - create your Access Tokens</small></div><br>

Choose the token type you need, in this example, you can choose read-only access because it is sufficient to open pull requests. Then type your token name in the blank space. Here, we type "image-to-text" as our token's name since we will use image-to-text model in this example later.

![[Step1-2.png]](../img/images-wendi/Step1-2.png)
<div align="center"><small>Select and name your new Access Token</small></div><br>

After token is created, don't forget to copy your API token and save it to a safe place. You won't be able to access it again after you click **done**.<br>

![[Step1-3.png]](../img/images-wendi/Step1-3.png)
<div align="center"><small>Copy and save your Access Token</small></div><br>

You can find the created token here.

![[Step1-4.png]](../img/images-wendi/Step1-4.png)
<div align="center"><small>Access Tokens example - an image-to-text token</small></div>

### Step 2: Choose a model you like

Go to the main page of Hugging Face, then click **Models**.

![[Step2.png]](../img/images-wendi/Step2.png)
<div align="center"><small>Hugging Face homepage - select the Models section</small></div><br>

On the next page, there are thousands of different models you can use. You can sort the models based on the function you need on the left side. You also can type the names of models to search for them.<br>

![[Step2-2.png]](../img/images-wendi/Step2-2.png)
<div align="center"><small>Find a model you like - sorting and search options on the left side</small></div><br>

Here, we use an image-to-text model called "blip-image-captioning-base" as an example. This AI model can descript the content image you provide. You can also use other models you like.<br>

![[Step2-3.png]](../img/images-wendi/Step2-3.png)
<div align="center"><small>Image-to-text model example - BLIP image captioning base</small></div>

### Step 3: Run the model in your application.

Using this model in your own app is quite easy. Here, we need to set up the API in your code. On Hugging Face, the model will provide the direct code to use it. First, you need to click **Deploy** on this page then click **Inference API (serverless)**.<br>

![[Step3.jpg]](../img/images-wendi/Step3.jpg)
<div align="center"><small>Select 'Inference API (serverless)' from the 'Deploy' dropdown box</small></div><br>

In the next window, you can choose any programming language you like. In this example, we choose Python as an example.<br>

![[Step3-2.png]](../img/images-wendi/Step3-2.png)
<div align="center"><small>Using Python as an example - choose a programming language and copy it</small></div><br>

Here is the code we use. You need to replace the "hf_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" token with yours. Then, you can insert this code into your own program.

```python 
import requests

API_URL = "https://api-inference.huggingface.co/models/Salesforce/blip-image-captioning-base"

headers = {"Authorization": "Bearer hf_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"}

def query(filename):

    with open(filename, "rb") as f:
        data = f.read()
    response = requests.post(API_URL, headers=headers, data=data)
    return response.json()

output = query("yourphoto.jpg")

print(output)
```

In this example, we used this cat photo as our input.

![[yourphoto.jpg]](../img/images-wendi/yourphoto.jpg)
<div align="center"><small>A cat photo as input (downloaded from Pexels on 17 Jul 2024)</small></div><br>

Then run the code using the command below and get the result from our Hugging Face model. Don't forget to change "app" to your file name. The result says "a cat sitting on a couch looking at the camera", which is an accurate and good description.

```python 
py app.py
```

![[Step3-3.png]](../img/images-wendi/Step3-3.png)
<div align="center"><small>The result generated by this image-to-text model</small></div><br>

Of course, we can enhance the input for our model by incorporating a UI, making it more visually appealing and user-friendly. However, the primary goal of this article is to share how to use the Hugging Face API, so we will not delve further into this topic.

## Conclusion

The Hugging Face API offers a powerful and efficient tool, enabling us to integrate thousands of pre-trained, mature models into our own software applications. This article provides a detailed guide on how to use the API, aiming to enhance the productivity of our user community. However, since anyone or any institution can upload their models to the platform, it is important to be mindful of the quality and accuracy of the models you choose, as they might impact your results.

## References

*Technical Support Documentation for Hugging Face - Get Started.* [Read me](https://huggingface.co/docs/api-inference/en/quicktour#overview).