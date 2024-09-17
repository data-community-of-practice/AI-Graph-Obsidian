
![math_intro](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/math-intro.png)

<div align="center" ><i>Source : mistral.ai</i></div>

# Author

Tarun Krishnan (**ORCID**: [0009-0006-6647-127X](https://orcid.org/0009-0006-6647-127X))

# Introduction

In the world of mathematics, problem-solving can often feel like navigating a complex maze. Whether you're a student struggling with calculus, a professional dealing with data analysis, or just someone who loves diving into the wonders of math, having the right tools at your disposal can make all the difference. Enter **MathΣtral** — a cutting-edge AI-powered platform designed to be your ultimate math buddy.

![math_kid](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/mathkid.webp)
<div align="center" ><i>Prompt Provided to DALL-E : "Child struggling with math homework."</i></div>

MathΣtral is more than just a tool; it’s a comprehensive companion that simplifies complex math concepts, offers step-by-step solutions, and makes learning math an engaging experience. Developed by the innovative team at Mistral, MathΣtral harnesses the power of advanced AI to bring you a personalized and interactive approach to mastering math.

We will first explore the features of **MathΣtral** to understand why this Generative AI stands out as the best choice for math enthusiasts. Finally, we'll dive into a step-by-step tutorial on how to integrate **MathΣtral** into Python, making math solutions easier than ever!
# Features of MathΣtral

#### 1. **Advanced Mathematical Reasoning**

MathΣtral is designed specifically for advanced mathematical reasoning and scientific discovery. It excels in complex, multi-step logical reasoning, making it an invaluable tool for tackling intricate mathematical problems.

#### 2. **Specialized STEM Focus**

Standing on the shoulders of Mistral 7B, MathΣtral specializes in STEM (Science, Technology, Engineering, and Mathematics) subjects. It provides state-of-the-art reasoning capabilities, achieving impressive results on industry-standard benchmarks like MATH and MMLU.

#### 3. **Lightweight and Device-Friendly**

MathΣtral is designed to be lightweight, with only 7 billion parameters, making it suitable for installation and operation on various devices, including personal computers and some mobile devices. Despite its advanced capabilities and large context window, the model maintains a manageable size, ensuring efficient use of computational resources. This allows you to leverage the power of MathΣtral for complex mathematical reasoning without needing access to high-end hardware, offering flexibility and convenience for users on the go.

#### 4. **High Performance on Benchmarks**

MathΣtral achieves notable performance metrics in its category, scoring 56.6% on the MATH benchmark and 63.47% on MMLU. With additional inference-time computation, it can score up to 68.37% on MATH with majority voting and 74.59% using a strong reward model among 64 candidates, demonstrating its robust problem-solving abilities.

![math_feat](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/math-feat.png)
<div align="center" ><i>MathΣtral MMLU performance difference by subject between MathΣtral 7B and Mistral 7B, Source : mistral.ai</i></div>

MathΣtral further demonstrates superior performance in mathematical reasoning across a wide range of topics compared to competitors such as DeepSeek Math 7B, Llama 3 8B, and Qwen2 7B. This exceptional capability provides yet another compelling reason to choose MathΣtral for advanced mathematical tasks.

![math_compare](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/math-compare.png)
<div align="center" ><i>MathΣtral Mathematical Reasoning Comparative Performance, Source : mistral.ai</i></div>
<div align="center" ><i> </i></div>
#### 5. **32k Context Window**

The model features a 32k context window, allowing it to handle and process large amounts of information efficiently. This capacity is crucial for solving complex mathematical problems that require considering extensive data or multiple steps.

#### 6. **Fine-Tuning Capabilities**

MathΣtral is an instructed model, which means it can be used as-is or fine-tuned for specific applications. It can be adapted to different mathematical tasks or integrated into various workflows, offering flexibility for users with diverse needs.

#### 7. **Open Source and Community Support**

MathΣtral is released under the Apache 2.0 license, making it freely accessible to the scientific community and encouraging collaborative efforts in advanced mathematical research. The model is available for download on platforms like HuggingFace and Ollama, and users can experiment with it using mistral-inference or customize it with mistral-finetune.

#### 8. **Collaboration with Academic Projects**

MathΣtral was developed in collaboration with Project Numina, highlighting its commitment to supporting academic research. It has been evaluated using GRE Math Subject Test problems curated by experts, ensuring its capabilities are well-aligned with educational and research needs.

#### 9. **Efficient Performance/Speed Trade-offs**

The development philosophy behind MathΣtral emphasizes achieving excellent performance while maintaining speed and efficiency. It serves as an example of building models tailored for specific purposes, ensuring that users get the best results without sacrificing computational resources.

# Step-by-Step Tutorial: How to Install and Use MathΣtral in Python

This guide will walk you through setting up and using MathΣtral in Python. We'll be using a Jupyter Notebook for this tutorial, but these steps should work in any Python environment.

#### Step 1: Set Up Your Hugging Face Account

To begin, you need a Hugging Face account. If you haven't created one yet, go to the [Hugging Face website](https://huggingface.co/), click on the "Sign Up" button in the top right corner, and fill in your details to register.

#### Step 2: Log In to Hugging Face in Your IDE

After setting up your account, you'll need to log in to Hugging Face through your IDE. First, install the Hugging Face Hub package by running:

```bash 
pip install huggingface_hub
```

Next, log in to your Hugging Face account using the following code in your Jupyter Notebook. This will prompt you to enter your Hugging Face authentication key during the login process.

```python
from huggingface_hub import notebook_login

notebook_login()
```

#### Step 3: Share Your Contact Information on Hugging Face

To access the MathΣtral model, you need to agree to share your contact information on the model's [Hugging Face page](https://huggingface.co/mistralai/Mathstral-7B-v0.1). This process uses the information from your Hugging Face account, so you don't need to re-enter anything.

![math_access](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/math-access.png)
<div align="center"><i>Source: huggingface.co</i></div>

#### Step 4: Implementation

Now that the basic setup is complete, let's proceed with the code to run the MathΣtral model.

**Install Necessary Packages**: First, install the required packages:
```bash 
pip install -U transformers accelerate bitsandbytes
```

**Set Up Quantization**: The following code sets up the `BitsAndBytesConfig` for 4-bit quantization. This allows the model to be loaded in a more memory-efficient manner, making it suitable for systems with limited resources.
```python
from transformers import AutoTokenizer, AutoModelForCausalLM, BitsAndBytesConfig

bnb_config = BitsAndBytesConfig(
    load_in_4bit=True,
    bnb_4bit_quant_type="nf4",
    bnb_4bit_use_double_quant=True,
)
```

**Load and Use the Model**: Now, you can load the MathΣtral model using the `transformers` library. This example demonstrates how to set up a text generation pipeline. The prompt is a question about the remaining amount of coffee in a cup, but you can modify it to ask anything else.
```python
from transformers import pipeline
import torch

# Load your model
checkpoint = "mistralai/Mathstral-7b-v0.1"
pipe = pipeline("text-generation", checkpoint, device_map="auto", torch_dtype=torch.bfloat16)

# Generate text with an increased maximum token limit
prompt = [{"role": "user", "content": "I have a 300ml cup of coffee. If I drink one-third of the cup, how much coffee in milliliters do I have left?"}]
output = pipe(prompt, max_new_tokens=200)  # Adjust max_new_tokens for longer or shorter responses

print(output[0]['generated_text'])
```

#### Output
Congratulations! After running the code, you should see an output from the MathΣtral model. The model not only provides the final answer but also includes an explanation of how it arrived at the result, giving insight into its reasoning process.

![math_result](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/math-result.png)
<div align="center"><i>Result from MathΣtral model</i></div> 

By following these steps, you can effectively set up and use the MathΣtral model in Python for various text generation tasks.
# Conclusion 

Diving into the MathΣtral model not only showcases the advancements in AI and natural language processing but also emphasizes the growing accessibility of these powerful tools. By following the steps outlined, you’ve engaged with a process that allows complex models to run efficiently on everyday hardware, making advanced AI more democratized than ever.

This journey reflects a larger movement in AI towards creating more inclusive and user-friendly technologies. As models like MathΣtral become easier to implement, they empower individuals and small teams to leverage cutting-edge technology without needing vast resources. This shift is not just about improving computational capabilities; it’s about enhancing our ability to explore, learn, and create in ways previously limited to large organizations.

In essence, working with MathΣtral is more than a technical exercise; it’s a glimpse into the future of how we interact with and harness artificial intelligence. It encourages us to think about how these tools can be integrated into various domains, from education to research and beyond, enhancing our capabilities and understanding of the world. As you continue exploring this field, consider the broader implications of AI accessibility and the new possibilities it brings to diverse fields and communities.

# References

1) “MathΣtral.” _Mistral.ai_, 16 July 2024, mistral.ai/news/mathstral/.
2) “Mistralai/Mathstral-7B-V0.1 · Hugging Face.” _Huggingface.co_, 2023, huggingface.co/mistralai/Mathstral-7B-v0.1. Accessed 16 Sept. 2024.
