Zijian Yang

ORCiD: 0009-0006-8301-7634

------

Breaking New Ground: Optimizing Prompts for Generating Minority Images with AI

Article link: https://arxiv.org/abs/2410.07838

📌This research explores a novel approach to enhance text-to-image (T2I) generation by focusing on creating minority instances—visuals that are underrepresented in typical outputs. With implications for data augmentation, fairness, and creative AI, the study addresses an essential challenge in modern AI-based generative models.

🔹T2I diffusion models are highly effective at converting text into detailed images but often generate outputs from high-density regions of data distributions, limiting diversity. Existing samplers like classifier-free guidance prioritize common instances, leaving unique, low-likelihood features underexplored. This study tackles the bias by introducing **MinorityPrompt**, an optimized prompt system designed to encourage the generation of rare and unique outputs.

🔹The **MinorityPrompt** framework uses a targeted optimization approach by adding learnable tokens to text prompts. These tokens dynamically update during inference, preserving the core meaning while encouraging the generation of uncommon visual features. Unlike traditional methods, this technique does not require fine-tuning of the entire T2I model, making it efficient and adaptable across different diffusion models.

🔹The study’s experiments demonstrate that MinorityPrompt significantly enhances the ability to generate rare features while maintaining visual quality and text alignment. For instance, it effectively mitigates demographic biases, such as age or racial stereotypes, often present in baseline T2I outputs. The results were validated using popular models like Stable Diffusion and SDXL-Lightning.

🔹This approach paves the way for more inclusive and diverse T2I generation. Beyond creative applications, it has potential use cases in AI fairness, enabling a broader range of visual representation. Looking ahead, further exploration into integrating MinorityPrompt with other generative frameworks could unlock new opportunities for diversity-focused AI tools.

Um, S., & Ye, J. C. (2024). MinorityPrompt: Text to Minority Image Generation via Prompt Optimization. [ArXiv.org](http://ArXiv.org). https://arxiv.org/abs/2410.07838