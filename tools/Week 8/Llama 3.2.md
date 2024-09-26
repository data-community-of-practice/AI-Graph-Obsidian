# Llama 3.2: Meta's Groundbreaking Multimodal AI Model 

![](https://imgur.com/CMdqMDD.png)
<div align="center"><small>Llama 3.2 <a href="https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/" target="_blank">Source</a></small></div>

## Author  
- Tohfa Siddika Barbhuiya (**ORCID**: [0009-0007-2976-4601](https://orcid.org/0009-0007-2976-4601))


Meta has released **Llama 3.2**, its latest advancement in large language models, introducing groundbreaking **multimodal capabilities** and improved **efficiency**. This guide explores the key features, improvements, and potential applications of this cutting-edge AI model, set to revolutionize the field of artificial intelligence.

## Introduction to Llama 3.2

Llama 3.2 is Meta's first open-source AI model capable of processing **both text and images**. This collection ranges from lightweight versions for edge devices to powerful multimodal models capable of sophisticated reasoning tasks.

## Key Features and Improvements

### Multimodal Capabilities
For the first time in the Llama series, the **11B and 90B models** support vision tasks. These models can:
- Process high-resolution images up to **1120x1120 pixels**
- Perform **image captioning**, visual reasoning, and document visual question answering
- Integrate **image-text retrieval** capabilities

### New Model Sizes
Llama 3.2 introduces four new models:
- **1B** and **3B** parameter models: Lightweight text-only versions for edge and mobile devices
- **11B** and **90B** parameter models: Larger versions with vision capabilities

![](https://imgur.com/81U0Qyc.png)
<div align="center"><small>Llama 3.2 1B and 3B Model sizes<a href="https://huggingface.co/blog/llama32" target="_blank">Source</a></small></div>

### Performance Enhancements
Despite their smaller size, the new models show impressive performance:
- The **3B model** matches or exceeds Llama 3.1 8B on tasks like tool use and summarization
- The **1B model** rivals larger models on summarization and re-writing tasks

![](https://imgur.com/ZzbyLFr.png)
<div align="center"><small>Llama 3.2 1B and 3B Model Performance <a href="https://huggingface.co/blog/llama32" target="_blank">Source</a></small></div>

### Architectural Innovations
Llama 3.2 incorporates significant architectural changes for its vision models:
- A novel **adapter architecture** integrates image encoder representations into the language model
- **Cross-attention layers** feed image encoder representations into the core language model

## Differences Between Llama 3.2 and Llama 3.1

Here are the key differences between **Llama 3.2** and its predecessor, **Llama 3.1**:

1. **Multimodal Capabilities**:
   - Llama 3.2 introduces **multimodal models** (11B and 90B) that can process both text and images.
   - Tasks include **image captioning**, visual reasoning, and document visual question answering.
   - Llama 3.1 lacked these vision capabilities.

2. **New Lightweight Models**:
   - Llama 3.2 introduces **1B** and **3B** parameter text-only models for **edge devices**.
   - Llama 3.1 did not offer such small models optimized for edge use.

3. **Performance Improvements**:
   - The **3B model** in Llama 3.2 matches or exceeds Llama 3.1 8B on summarization tasks.
   - The **1B model** performs well on summarization and re-writing tasks, similar to larger models.

4. **Architectural Changes**:
   - Llama 3.2 incorporates a new **adapter architecture** for vision models, integrating image encoder representations.

5. **Efficiency and Optimization**:
   - Llama 3.2 offers **reduced latency** and improved performance, with techniques like **pruning** and **distillation**.

6. **Availability and Deployment**:
   - Llama 3.2 is available on platforms like **Amazon Bedrock**, **Hugging Face**, and Meta's Llama website.
   - Meta introduced **Llama Stack Distribution** for easier deployment.

7. **Safety Features**:
   - Includes updated **Llama Guard** (Llama-Guard-3-11B-Vision) for moderating image-text inputs and outputs.

8. **Context Length**:
   - Both Llama 3.1 and 3.2 support a **128K token context length**.


## Efficiency and Optimization
- **Improved efficiency** for AI workloads.
- Techniques like **pruning** and **distillation** create smaller, faster models.

## Multilingual Support
Llama 3.2 expands its multilingual capabilities, officially supporting eight languages:
- **English**
- **German**
- **French**
- **Italian**
- **Portuguese**
- **Hindi**
- **Spanish**
- **Thai**

## Vision models

As the first Llama models capable of handling vision tasks, the 11B and 90B models required a new architecture designed to support image reasoning.

To enable image input, adapter weights were trained to integrate a pre-trained image encoder with the pre-trained language model. The adapter uses cross-attention layers to feed the image encoder's representations into the language model. These adapters were trained on text-image pairs to align the image and text representations. While training the adapters, the image encoder parameters were updated, but the language model's parameters remained unchanged to preserve its text-only capabilities, making it a seamless replacement for Llama 3.1 models.

The training process followed multiple stages, starting with pretrained Llama 3.1 text models. First, image adapters and encoders were added and pretrained on large-scale noisy image-text pairs. Then, the models were trained on medium-scale, high-quality, domain-specific, and knowledge-enhanced image-text pairs.

For post-training, a similar approach to the text models was used, involving alignment through supervised fine-tuning, rejection sampling, and direct preference optimization. Synthetic data generation played a key role, with the Llama 3.1 model filtering and augmenting questions and answers based on in-domain images. A reward model was employed to rank candidate answers for fine-tuning data. Additionally, safety mitigation data was incorporated to ensure the model maintained a high level of safety while remaining helpful.

The final result is a set of models that can process both image and text prompts, allowing for a deeper understanding and reasoning of the two combined inputs. This marks another step in enhancing Llama models with more advanced capabilities.

## Lightweight models

As we talked about with Llama 3.1, powerful teacher models can be utilized to create smaller models with enhanced performance. The team applied two techniques—pruning and distillation—to the 1B and 3B models, making them the first highly capable, lightweight Llama models that can efficiently run on devices.

Pruning helped reduce the size of existing Llama models while retaining as much knowledge and performance as possible. For the 1B and 3B models, structured pruning was applied in a single-shot process from the Llama 3.1 8B model. This involved systematically removing parts of the network and adjusting weights and gradients to create a smaller, more efficient model that still maintained the original performance.

Knowledge distillation transfers knowledge from a larger model to a smaller one, allowing the smaller model to achieve better performance than training from scratch. For the 1B and 3B models in Llama 3.2, logits from the Llama 3.1 8B and 70B models were incorporated during the pre-training stage, where outputs (logits) from the larger models were used as token-level targets. After pruning, knowledge distillation was applied to further recover and improve the model's performance.

## Benchmarks

while the instruct models were evaluated across three popular benchmarks that measure instruction-following and correlate well with the LMSYS Chatbot Arena: IFEval, AlpacaEval, and MixEval-Hard. These are the results for the base models, with Llama-3.1-8B included as a reference:

![](https://imgur.com/tV0B5ec.png)
<div align="center"><small>Llama 3.2 Benchmarks <a href="https://huggingface.co/blog/llama32" target="_blank">Source</a></small></div>


Remarkably, the 3B model is as strong as the 8B one on IFEval! This makes the model well-suited for agentic applications, where following instructions is crucial for improving reliability. This high IFEval score is very impressive for a model of this size.

![](https://imgur.com/xNEr3uH.png)
<div align="center"><small>Llama 3.2 Vision Instruction tuned benchmarks <a href="https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/" target="_blank">Source</a></small></div>

Here's the table structure in Markdown format:

| Benchmark | Llama 3.2 1B | Llama 3.2 3B | Gemma 2 2B IT | Phi-3.5-mini IT |
|-----------|--------------|--------------|---------------|-----------------|
| MMLU | 49.3 | 63.4 | 57.8 | 69.0 |
| Open-rewrite eval | 41.6 | 40.1 | 31.2 | 34.5 |
| TLDR9+ | 16.8 | 19.0 | 13.9 | 12.8 |
| IFEval | 59.5 | 77.4 | 61.9 | 59.2 |
| BPCLv2 | 25.7 | 67.0 | 27.4 | 58.4 |
| Nexus | 13.5 | 34.3 | 21.0 | 26.1 |
| GSMBK | 44.4 | 77.7 | 62.5 | 86.2 |
| MATH | 30.6 | 48.0 | 23.8 | 44.2 |
| ARC Challenge | 59.4 | 78.6 | 76.7 | 87.4 |
| GPQA | 27.2 | 32.8 | 27.5 | 31.9 |
| Hellaswag | 41.2 | 69.8 | 61.1 | 81.4 |
| InfiniteBench/En.MC | 38.0 | 63.3 | — | 39.2 |
| InfiniteBench/En.QA | 20.3 | 19.8 | — | 11.3 |
| NIH/Multi-needle | 75.0 | 84.7 | — | 52.7 |
| MGSM | 24.5 | 58.2 | 40.2 | 49.8 |



## How to Download and Run Llama 3.2 Locally 

For this project, we are using Llama-3.2-1B-Instruct model on Mac.

### Llama.cpp & Llama-cpp-python

**Llama.cpp** is the go-to framework for all things cross-platform on-device ML inference. Meta provides quantized **4-bit** and **8-bit** weights for both the **1B** and **3B** models in this collection. The community is encouraged to embrace these models and create additional **quantizations** and **fine-tunes**. You can find all the quantized **Llama 3.2** models [here](https://huggingface.co).

## Installing Llama.cpp

To use these checkpoints with **llama.cpp**, you need to install it. Here's how to install **llama.cpp** via **Homebrew** (works on Mac and Linux):

```bash
brew install llama.cpp
```

### Running Llama 3.2 with Llama.cpp
Once installed, you can use the CLI to run a single generation or invoke the llama.cpp server, which is compatible with the OpenAI messages specification.

Running a Single Generation with CLI
You can use the following command to generate text with Llama 3.2:

```bash
llama-cli --hf-repo hugging-quants/Llama-3.2-1B-Instruct-Q4_K_M-GGUF --hf-file llama-3.2-1b-instruct-q4_k_m.gguf -p "The meaning to life and the universe is"
```

![](https://imgur.com/0iAySis.png)
<div align="center"><small>Llama 3.2 1B output</small></div>

```bash
llama-cli --hf-repo hugging-quants/Llama-3.2-1B-Instruct-Q4_K_M-GGUF --hf-file llama-3.2-1b-instruct-q4_k_m.gguf -p "The meaning to life and the universe is"
```

![](https://imgur.com/Jpc6IHi.png)
<div align="center"><small>Llama 3.2 1B output</small></div>

## Online Demo

You can experiment with the three Instruct models in the following demos:

<a href="https://huggingface.co/spaces/huggingface-projects/llama-3.2-vision-11B" target="_blank">Gradio Space with Llama 3.2 11B Vision Instruct</a>

<a href="https://huggingface.co/spaces/huggingface-projects/llama-3.2-3B-Instruct" target="_blank">Gradio-powered Space with Llama 3.2 3B</a>

![](https://imgur.com/i4hxdd5.png)
<div align="center"><small>Llama 3.2 online demo query<a href="https://huggingface.co/spaces/huggingface-projects/llama-3.2-vision-11B" target="_blank">Source</a></small></div>

![](https://imgur.com/DlXgPEs.png)
<div align="center"><small>Llama 3.2 online demo output <a href="https://huggingface.co/spaces/huggingface-projects/llama-3.2-vision-11B" target="_blank">Source</a></small></div>

## Applications and Use Cases

Llama 3.2 is versatile, with potential applications such as:
1. **Content Creation**: High-quality text generation and image analysis for creative tasks.
2. **Visual AI Assistants**: Build chatbots that understand and discuss visual content.
3. **Document Analysis**: Extract information from document images, receipts, and charts.
4. **E-commerce**: Improve product descriptions and visual search capabilities.
5. **Healthcare**: Assist in medical image analysis and report generation.
6. **Education**: Create interactive learning experiences with text and visual elements.


## Future Implications

Llama 3.2 represents a significant advancement in open-source AI:
- It could lead to **more sophisticated AI assistants** capable of understanding and generating both text and visual content.
- Its **smaller models** enable improved **on-device AI** applications.
- It paves the way for advancements in **multilingual** and **cross-modal AI** understanding.


## Conclusion

Llama 3.2 marks a major milestone in large language models. With its **multimodal capabilities**, improved **efficiency**, and enhanced performance, Meta has created powerful tools that can push the boundaries of AI. Whether you're a developer, researcher, or business leader, leveraging the capabilities of Llama 3.2 could be key to staying at the forefront of AI technology in 2024 and beyond.

## References

[1] Llama Models, "Llama 3.2 Model Card," GitHub, https://github.com/meta-llama/llama-models/blob/main/models/llama3_2/MODEL_CARD.md.

[2] Hugging Face, "Llama 3.2 Vision 11B," Hugging Face, https://huggingface.co/spaces/huggingface-projects/llama-3.2-vision-11B.

[3] Hugging Face, "Llama 3.2," Hugging Face, https://huggingface.co/blog/llama32.

[4] Meta AI, "Llama 3.2 Connect 2024: Vision, Edge, and Mobile Devices," Meta AI, https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/.
