# NousResearch’s Hermes 3 - A Breakthrough in Generalist Instruct Models

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/Hermes3.png)
<div align="center"><small>Hermes 3 by NousResearch <a href="https://nousresearch.com/hermes3/" target="_blank">Source</a></small></div>

## Author  
- Tohfa Siddika Barbhuiya (**ORCID**: [0009-0007-2976-4601](https://orcid.org/0009-0007-2976-4601))

## Introduction

NousResearch's Hermes 3 is a breakthrough in Generalist Instruction Models, offering advancements in Language Models and versatile AI Capabilities. Hermes 3 contains advanced long-term context retention and multi-turn conversation capability, complex roleplaying and internal monologue abilities, and enhanced agentic function-calling. Hermes 3 training data aggressively encourages the model to follow the system and instruction prompts exactly and in an adaptive manner. Hermes 3 was created by fine-tuning Llama 3.1 8B, 70B and 405B, and training on a dataset of primarily synthetically generated responses. These models are not only powerful but also uniquely aligned to follow system and instruction prompts with unparalleled precision and neutrality. The model boasts comparable and superior performance to Llama 3.1 while unlocking deeper capabilities in reasoning and creativity.This article deep dives into the innovative features of Hermes 3, its advanced capabilities, and its impact on the field of AI. This Generalist AI System showcases Intelligent Conversational Agents and Adaptive AI Algorithms, enabling Personalized AI Assistance and AI-driven Task Completion. Hermes 3 has demonstrated impressive Performance Benchmarks, making it a valuable addition to the NousResearch AI Ecosystem. As an Instructable AI Assistant, Hermes 3 can be seamlessly integrated into various Workflows, driving Productivity Enhancement and Automation Solutions across a wide range of applications.

## Model Overview and Key Features

Hermes 3, particularly its flagship 405B model, is designed to excel in a variety of complex tasks. The model's advanced reasoning and creative capabilities are complemented by several key features that set it apart from its predecessors:

- **Advanced Agentic Capabilities**: Hermes 3 demonstrates refined autonomy, making it capable of handling complex, goal-oriented tasks with minimal supervision.
- **Enhanced Roleplaying and Reasoning**: The model excels in maintaining coherent, contextually appropriate interactions over multiple turns, making it ideal for applications in virtual assistants and interactive storytelling.
- **Improved Long-Context Coherence**: Hermes 3 maintains the flow of conversation and context over extended dialogues, crucial for long-form content creation and analysis.
- **Structured Output and Function Calling**: With advanced capabilities in generating structured outputs like JSON and invoking external tools, Hermes 3 is a versatile tool for developers looking to integrate AI into existing systems.

## Innovative Features of Hermes 3

Hermes 3 introduces several cutting-edge features that enhance its ability to solve complex problems:

- **Structured Output with XML Tags**: The model can generate well-organized outputs using XML tags, facilitating structured communication.
- **Intermediate Processing using Scratchpads**: Hermes 3 uses scratchpads for intermediate steps, ensuring transparency and accuracy in decision-making.
- **Transparent Decision-Making through Internal Monologues**: The model provides insight into its reasoning process through internal monologues, making its decision-making more understandable.
- **Visual Communication with Mermaid Diagrams**: Hermes 3 can generate visual representations of information using Mermaid diagrams, enhancing clarity and comprehension.
- **Step-Labeled Reasoning and Planning**: The model labels each step in its reasoning and planning process, offering a clear roadmap of its problem-solving approach.

## Enhanced Tool Use and Retrieval Augmented Generation (RAG)

Hermes 3 use cases are it excels in tool use and retrieval augmented generation (RAG) through the Hermes Function Calling standard. This standard leverages specific JSON schemas to define and invoke tools, significantly enhancing the model’s ability to manage complex tasks and communicate solutions effectively across various domains.

## Data Mixture and Training Recipe

The Hermes 3 dataset is a carefully curated collection of 390 million tokens, covering a wide range of domains. This diverse mixture includes:

- **270M Response Tokens (69%)**: Ensuring robust responses across different scenarios.
- **120M Instruction Tokens (31%)**: Fine-tuning the model's ability to follow complex instructions.

The training process of Hermes 3 is executed in two phases:

- **Supervised Fine-Tuning (SFT)**: This phase optimizes the model's response quality and accuracy.
- **Direct Preference Optimization (DPO)**: DPO offers further refinement, particularly enhancing the performance of the 8B model.

## Hermes 3 performance benchmarks

Hermes 3 has undergone rigorous testing against a variety of benchmarks, showcasing its competitive, if not superior, capabilities compared to Llama-3.1 Instruct models. The Hermes 3 Technical Report provides detailed comparisons and analyses, highlighting the model's strengths and areas for improvement.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/Hermes3evaluations.png)
<div align="center"><small>Hermes 3 performance evaluation <a href="https://nousresearch.com/wp-content/uploads/2024/08/Hermes-3-Technical-Report.pdf" target="_blank">Source</a></small></div>

## Prompt Format and Inference

Hermes 3 employs the ChatML prompt format, which facilitates structured and intuitive multi-turn chat dialogues. Key aspects include:

- **System Prompts**: These allow for high steerability, enabling users to define roles, stylistic choices, and interaction rules.
- **Function Calling and Structured Outputs**: The model's training on specific system prompts supports function calling, making it an effective tool for complex data retrieval and processing.

With its massive 405 billion parameters, Hermes 3 requires significant computational resources. NeuralMagic's FP8 quantization method reduces the model's VRAM requirements, making it more accessible for large-scale inference tasks.

## Hermes 3 - Llama-3.1 8B - Install and Test Locally

I have used Anaconda and Jupyter notebook for this project.
Open your Anaconda prompt.

1. Create a new Conda environment named "hermes" with Python 3.11
```bash
conda create -n hermes python=3.11 -y
```

2. Activate the "hermes" Conda environment
```bash
conda activate hermes
```

3. Install PyTorch in the "hermes" environment
```bash
conda install pytorch torchvision torchaudio cudatoolkit=11.8 -c pytorch
```

4. Upgrade the Transformers library to the latest version
```bash
pip install --upgrade transformers
```

5. Install the Accelerate library and Hugging Face Hub
```bash
pip install accelerate huggingface hub
```

6. Install Jupyter Notebook in the "hermes" environment
```bash
conda install jupyter -y
```

7. Uninstall the charset_normalizer package if it is installed.
```bash
pip uninstall charset_normalizer -y
```

8. Reinstall the charset_normalizer package to ensure you have the correct version.
```bash
pip install charset_normalizer 
```

9. Launch Jupyter Notebook to start creating and managing your notebooks.
```bash
jupyter notebook 
```
Now create a new notebook and start working

10. Launch Jupyter Notebook to start creating and managing your notebooks.
```python
jupyter notebook 
```

11. Import essential libraries for working with transformers and PyTorch
```python
import transformers
import torch
from IPython.display import Markdown,display
```

12. Set up a text generation pipeline using the Hermes-3 model from Hugging Face Transformers
```python
import transformers

model_id = "NousResearch/Hermes-3-Llama-3.1-8B"

pipeline = transformers.pipeline(
    "text-generation",
    model=model_id,
    model_kwargs={"torch_dtype": torch.bfloat16},
    device_map="auto"
)
```

13. Generate a response from the Hermes-3 model based on a user quiz query and display the output
```python
messages = [
    {"role": "system", "content": "You are helpful assistant!"},
    {"role": "user", "content": "which is the largest sand island in the world and in which country is it?" }
]

outputs = pipeline(messages, max_new_tokens=1024)
output_text = outputs[0]["generated_text"][-1]['content']
display(Markdown(output_text))
```
Response:
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/Hermes3output.png)
<div align="center"><small>Image generated from the desktop of Tohfa Siddika Barbhuiya</small></div>

14. Solve a math problem using the Hermes-3 model and display the solution
python
prompt = """
A notebook and pen costs $2.20. The notebook costs $1.00 more than the pen. How much doe sthe pen costs"
"""

messages = [
    {"role": "system", "content": "You are helpful assistant!"},
    {"role": "user", "content": prompt }
]

outputs = pipeline(messages, max_new_tokens=1024)
output_text = outputs[0]["generated_text"][-1]['content']
display(Markdown(output_text))

Response:
![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian/img/Hermes3outputmaths.png)
<div align="center"><small>Image generated from the desktop of Tohfa Siddika Barbhuiya</small></div>

## Training Focus Areas

The training of Hermes 3 focused on several key areas to enhance its capabilities:

- **Agentic Capabilities**: Improved autonomy in complex scenarios.
- **Roleplaying**: Enhanced understanding and maintenance of different personas.
- **Reasoning**: Significant advancements in logical problem-solving.
- **Multi-turn Conversation**: Improved coherence and context across extended dialogues.
- **Long Context Coherence**: Better relevance maintenance over longer text passages.

## Conclusion

Hermes 3 is a groundbreaking advancement in the field of generalist instruct models. With its cutting-edge features, enhanced tool use capabilities, and robust training, Hermes 3 sets a new standard for AI models in various domains. Whether you're a researcher, developer, or AI enthusiast, Hermes 3 AI model offers powerful tools and functionalities that can drive innovation and elevate your projects to new heights. For more details on its capabilities, benchmarks, and usage, refer to the Hermes 3 Technical Report.

## References

Nous Research, "Hermes 3," Nous Research. [Online]. Available: https://nousresearch.com/hermes3/. [Accessed: 21-Aug-2024].

Nous Research, "Hermes 3 Collection," Hugging Face. [Online]. Available: https://huggingface.co/collections/NousResearch/hermes-3-66bd6c01399b14b08fe335ea?source=post_page-----cdbe2cb27a2d--------------------------------. [Accessed: 21-Aug-2024].

Nous Research, "Hermes 3 Technical Report," Aug. 2024. [Online]. Available: https://nousresearch.com/wp-content/uploads/2024/08/Hermes-3-Technical-Report.pdf. [Accessed: 21-Aug-2024].

