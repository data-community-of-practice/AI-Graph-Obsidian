
### Introduction

In recent times, the battle for developing the most capable language model has intensified, with many big tech companies getting deeply involved in generative AI. This has led to the creation of massive models, some boasting even trillions of parameters. There is a common misconception that 'bigger is better,' meaning that people often think that the more parameters a model has or the more training data it is fed, the better it will perform. Enter Microsoft with their latest generative AI model, 'Phi-3', that has proved to have better performance on standard open-source benchmarks (that measure the model’s reasoning ability) like MMLU and MT-bench than popular competitors Mixtral 8x7B and GPT-3.5, which both contain billions more parameters than Phi-3.
### Exploring Phi-3

Microsoft released 4 variants of Phi-3:
- **Phi-3-mini**: This model has 3.8 billion parameters. It is designed for applications that need to run locally on a device, where tasks don't require extensive reasoning or where quick responses are necessary. This model was tested on an iPhone 14 with an A16 Bionic chip in fully offline mode and achieved more than 12 tokens per second.
- **Phi-3-vision:** A 4.2 billion parameter model based on phi-3-mini which possesses strong reasoning capabilities for image and text prompts.
- **Phi-3-small**: This version contains 7 billion parameters. It strikes a balance between performance and computational efficiency, making it suitable for tasks that need more capacity than the mini version but still benefit from a compact model size.
- **Phi-3-medium**: This is the largest in the Phi-3 family, with 14 billion parameters. It is more suited for complex tasks that involve advanced reasoning, data analysis, and understanding of context​. 

Now that we know the different versions of Phi-3 let us talk about 
