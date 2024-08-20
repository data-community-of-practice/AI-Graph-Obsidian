
![Mamba](https://mistral.ai/images/news/codestral-mamba/codestral-mamba.png)
<div align="center" ><i>Source : mistral.ai</i></div>

# Author

Tarun Krishnan (**ORCID**: [0009-0006-6647-127X](https://orcid.org/0009-0006-6647-127X))

# Introduction

Before the rise of Large Language Models (LLMs), coders often spent countless hours debugging their code or searching for solutions to complex problems on platforms like Stack Overflow. Finding the right answer was often a tedious process, requiring users to sift through hundreds of pages, hoping to stumble upon the solution. However, with the advent of LLMs like ChatGPT, those long, tiresome days are becoming a thing of the past. Now, developers can simply input their code into a prompt and receive quick, accurate guidance on how to complete or fix it.

![Mamba](https://easy-peasy.ai/cdn-cgi/image/quality=80,format=auto,width=700/https://fdczvxmwwjwpwbeeqcth.supabase.co/storage/v1/object/public/images/5dc57da3-fd63-47a6-80cd-0ba08c457be7/ed2552ab-99c9-4ee8-a94e-710ac2cc22a5.png)
<div align="center" ><i>Source : Easy-Peasy.AI</i></div>


In May 2024, Mistral AI made waves in the AI community with the release of "Codestral," a model designed specifically for code generation. It quickly set a new standard, boasting unparalleled performance on benchmarking tests. The only drawback, if any, was its size: with 22 billion parameters, Codestral required substantial storage space and computing resources, making it challenging to run on personal devices.

Probably in response to community feedback, Mistral AI introduced a more lightweight version called "Codestral Mamba." Despite its reduced size, Codestral Mamba delivers performance comparable to its predecessor—if not better in some coding benchmarks—offering developers a powerful tool that is both accessible and efficient.

# Features of Codestral Mamba

Lets look at reasons to why you should think about using Codestral Mamba instead of other LLM competitors like Chatgpt or Gemini:

1) **Specialized in Code Generation**: Codestral Mamba is specifically designed with code generation in mind. Unlike general-purpose language models, it has been fine-tuned on a vast dataset of programming languages, algorithms, and coding best practices. This specialization enables Codestral Mamba to understand complex coding tasks, generate high-quality code snippets, and even provide detailed explanations and solutions for challenging coding problems. Whether you're debugging, refactoring, or writing new code, Codestral Mamba excels at delivering precise, context-aware code outputs tailored to your needs.

   As illustrated in the below image, Codestral Mamba outperforms many similarly sized popular code generation models, such as CodeGemma and CodeLlama (with 7 billion parameters), across most benchmark metrics. Remarkably, it also matches or surpasses the performance of much larger models, including Codestral and CodeLlama (with 34 billion parameters), in several benchmarks.

![Mamba Compare](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/mamba-compare.png)
<div align="center" ><i>Codestral Mamba Coding Capabilities via mistral.ai</i></div>



2) **Fast Response Times**: One of the standout features of Codestral Mamba is its use of Mamba models, which differ from traditional Transformer models by offering linear time inference and the ability to model sequences of infinite length. This means users can engage with the model extensively, receiving quick responses regardless of input length. This efficiency is particularly valuable for code productivity, as Codestral Mamba has been trained with advanced code and reasoning capabilities, allowing it to perform on par with state-of-the-art Transformer-based models.

3) **Massive In-Context Capabilities**: Codestral Mamba has demonstrated impressive in-context retrieval capabilities, handling up to 256,000 tokens with ease. This extensive capacity allows the model to effectively manage and retrieve large volumes of context, making it an excellent local code assistant. Whether you’re working on extensive codebases or require detailed context for complex coding tasks, Codestral Mamba provides reliable and efficient support, ensuring accurate and contextually relevant responses.

4) **Deployment** : Codestral Mamba can be deployed using the mistral-inference SDK, which leverages reference implementations from Mamba’s GitHub repository. Additionally, it supports deployment through TensorRT-LLM for optimized performance. For local inference, the Mistral team has advised us to keep an eye out for upcoming support in llama.cpp as of the time of this article. Further, the raw model weights are available for download on HuggingFace.

5) **Accessibility**: For convenient testing, Codestral Mamba is accessible on la Plateforme (codestral-mamba-2407), alongside its larger counterpart, Codestral 22B. Codestral Mamba is offered under the Apache 2.0 license, while Codestral 22B is available under a commercial license for self-deployment or a community license for testing. This flexibility in licensing and deployment options ensures that both models can be integrated and tested effectively across various environments.

# Setting Up and Accessing Codestral Mamba

As of the time of this article, Codestral Mamba is not available for download through Ollama but if you wish to download the bigger version "Codestral", you can install it using this link : [Codestral Ollama Download](https://ollama.com/library/codestral)

We shall cover how to access Codestral Mamba through their API in python in this article: 
## Get an API Key

To access the Codestral Mamba through an API , you'll first need an API key. Here’s how to get one:

1. First go to the [Mistral AI sign-up page](https://auth.mistral.ai/ui/login?flow=098263c7-e157-460d-8dc8-e1052af92e5b) and create an account.

2. Next, navigate to the API Keys tab [Mistral AI API Key Workspace ](https://console.mistral.ai/api-keys/). Click Create new key to generate your API key. 

![Mamba API ](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/mamba-api1.png)
<div align="center" ><i>Mistral AI API Key Workspace</i></div>

[Mamba API 2](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/mamba-api2.png)
<div align="center" ><i>Mistral AI API Key Creation</i></div>

3. Make sure you save your API Key somewhere, you'll be needing it in the next step!

## Python Implementation

### Installing Necessary Packages

For this implementation, you only need to install the `mistralai` package. You can download it in your terminal using the following command:

```bash 
pip install mistralai
```

### Running the Python Code

#### Basic Imports

First, we need to import `os` and `Mistral` from the `mistralai` package that we just installed.

```python
import os
from mistralai import Mistral
```

#### Calling Mistral's API

Next, add the API Key you copied in the previous step and assign it to the `api_key` variable. Set the model name to `'codestral-mamba-latest'` to call the latest version of Codestral Mamba while making the request through the API. Finally, instantiate Mistral as a client by passing in the API key.

```python
api_key = 'INSERT YOUR API KEY HERE'
model = "codestral-mamba-latest"
client = Mistral(api_key=api_key)  
```

#### Sending in a Prompt

In the code below, simply write what you want Codestral Mamba to help you with (a.k.a. a prompt) and assign it to the `content` variable. You should receive a response through `chat_response`, which can be displayed by printing `chat_response.choices[0].message.content`.

```python
chat_response = client.chat.complete(
    model= model,
    messages = [
        {
            "role": "user",
            "content": "Write a code to find the prime numbers from 1 to 10",
        },
    ]
)
print(chat_response.choices[0].message.content)
```
#### Entire Code Put Together

```python
#Basic imports
import os
from mistralai import Mistral

#Adding Your API KEY
api_key = 'INSERT YOUR API KEY HERE'

#Model Name
model = "codestral-mamba-latest"

#Calling Mistral's API
client = Mistral(api_key=api_key)  

#Obtaining the responses from Codestral Mamba
chat_response = client.chat.complete(
    model= model,
    messages = [
        {
            "role": "user",
            #Write your desired prompt
            "content": "Write a code to find the prime numbers from 1 to 10",
        },
    ]
)

#Displays Codestral Mamba's Response
print(chat_response.choices[0].message.content)
```
## Testing Codestral Mamba's Response

I wrote a simple prompt asking Codestral Mamba to "Write a code to find the prime numbers from 1 to 10," and it returned the Python code shown in the image below, which successfully identified the prime numbers from 1 to 10.
[Mamba Output](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/mamba-output.png)
<div align="center" ><i>Codestral Mamba Sample Output</i></div>

It also provided an explanation of the generated code, as seen in the text box below.

```Explanation
This code first defines an empty list `primes` to store the prime numbers. It then iterates over each number from 1 to `n`. If the number is greater than 1, it checks if it's divisible by any number between 2 and itself. If it is, it's not a prime number and the loop breaks. If it's not divisible by any number, it's a prime number and is added to the `primes` list. After all numbers are checked, the list of primes is returned. Finally, the function is called with `n` set to 10 and the result is printed.
```
# Conclusion

Codestral Mamba represents a significant leap forward in making powerful code generation tools accessible to a broader audience, offering high performance in a compact, efficient package. Its ability to handle complex tasks with speed and accuracy, coupled with the ease of deployment, underscores the importance of continuous innovation in AI. As developers increasingly rely on AI-driven tools to enhance productivity and creativity, Codestral Mamba stands out not just as a technical achievement but as a symbol of the evolving relationship between humans and machines, where advanced capabilities are made available without sacrificing accessibility or efficiency.

# References

1) AI, Mistral. “Codestral Mamba.” _Mistral.ai_, 16 July 2024, mistral.ai/news/codestral-mamba/. Accessed 20 Aug. 2024.

2) “Mistralai/Mamba-Codestral-7B-V0.1 · Hugging Face.” _Huggingface.co_, 2024, huggingface.co/mistralai/Mamba-Codestral-7B-v0.1. Accessed 20 Aug. 2024.



