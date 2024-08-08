# Technical Guide to use Stability AI API

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/Stability_AI.png)
<div align="center"><small>Image from <a href="https://www.pymnts.com/acquisitions/2023/report-stability-ai-positioning-itself-for-acquisition/" target="_blank">Source</a></small></div>

## Author  
- Tohfa Siddika Barbhuiya (**ORCID**: [0009-0007-2976-4601](https://orcid.org/0009-0007-2976-4601)) 

## What is Stability AI and Its API?
Stability AI is a leading provider of artificial intelligence and machine learning solutions that focuses on developing advanced models for a range of applications. Their suite of services includes state-of-the-art AI models and APIs that facilitate various tasks such as image generation, natural language processing, and more. This guide will introduce you to Stability AI, its API, its benefits, and how to use it effectively. The Stability AI API provides programmatic access to their AI models. It allows developers to leverage Stability AI's powerful algorithms for tasks such as image generation, text analysis, and more. By integrating this API into your applications, you can harness the capabilities of advanced AI models without needing to build them from scratch.

# Why Use Stability AI API?

- **Advanced Models**: Access cutting-edge AI models that are continually improved by Stability AI.
- **Ease of Integration**: Simplify the integration of AI functionalities into your applications with a straightforward API.
- **Scalability**: Easily scale your applications without managing the underlying infrastructure.
- **Cost-Effective**: Pay only for the API usage, avoiding the costs associated with developing and maintaining AI models in-house.

# How to Use Stability AI API

## Sign Up and Get Your API Key

1. Register/login on the <a href="https://platform.stability.ai/" target="_blank">Stability AI</a>. You get 25 credits for free on sign up.
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/stability_ai_credits.png)
<div align="center"><small>Image generated using Stability AI API Key of Tohfa Siddika Barbhuiya</small></div>

2. Obtain your API key from the API section of your account dashboard, copy it and save it somewhere for use in upcoming step.
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/API_key_copy.png)
<div align="center"><small>Image generated using Stability AI API Key of Tohfa Siddika Barbhuiya</small></div>


## Install Required Libraries

For Python, open VS Code. Create new folder and file named app.py.
Open its terminal and install

Install the `requests` library:

```bash
pip install requests
```
If you are using Python 3 versions then use the below code to install `requests` library.

```bash
pip3 install requests
```

## Make API Requests

Use the API key to authenticate requests. Here’s an example using Python:

```python
import requests

response = requests.post(
    "https://api.stability.ai/v2beta/stable-image/generate/ultra",
    headers={
        "authorization": "*******Enter your API Key here*******",
        "accept": "image/*"
    },
    files={"none": ''},
    data={
        "prompt": "A distant exoplanet with a stunning ring system, glowing auroras, and a futuristic spaceship landing on its surface.",
        "output_format": "webp",
    },
)

if response.status_code == 200:
    with open("./lighthouse.webp", 'wb') as file:
        file.write(response.content)
else:
    raise Exception(str(response.json()))
```

Open the terminal and run the code.
```bash
python app.py
```
If you are using Python 3 versions then use the below code to run the script.

```bash
pyhton3 app.py
```
## Output

Outputs will be generated as per the prompt.

For prompt: "A distant exoplanet with a stunning ring system, glowing auroras, and a futuristic spaceship landing on its surface.", output generated is shown below.
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/spacecraft.png)
<div align="center"><small>Image generated from the desktop of Tohfa Siddika Barbhuiya</small></div>


For prompt: "Lighthouse on a cliff overlooking the ocean", output generated is shown below.
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/cliff.png)
<div align="center"><small>Image generated from the desktop of Tohfa Siddika Barbhuiya</small></div>

## Handle Responses
Check the API documentation for details on the response structure and how to handle the data returned.

## Applications

There are multiple applications, some of which are listed below

- **Image Generation**: Create high-quality images from text prompts or other inputs.
- **Text Analysis**:Analyze and generate text for various purposes, including content creation and data extraction.
- **Custom Models**: Develop tailored AI solutions for specific business needs.

## Conclusion
The Stability AI API offers powerful and scalable AI solutions that can significantly enhance your applications. By following the steps to integrate the API, you can leverage advanced AI capabilities with ease and efficiency. Understanding the billing structure and monitoring your usage will help you manage costs effectively while taking full advantage of Stability AI’s offerings.