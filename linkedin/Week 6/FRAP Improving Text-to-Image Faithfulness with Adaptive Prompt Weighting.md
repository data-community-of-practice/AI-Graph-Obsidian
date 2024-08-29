FRAP: Improving Text-to-Image Faithfulness with Adaptive Prompt Weighting

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 This paper addresses the challenge of ensuring prompt-image alignment in text-to-image (T2I) diffusion models, particularly in generating images that are both faithful to the provided text prompts and realistic in appearance. The proposed method, FRAP, introduces an adaptive approach for adjusting prompt weights during the Reverse Generative Process (RGP) to improve both faithfulness and authenticity of the generated images. The study compares FRAP with other existing methods and demonstrates its effectiveness in generating images with better prompt-image alignment and reduced inference latency.

Article link: https://arxiv.org/abs/2408.11706

🔹 The paper tackles the problem of prompt-image alignment in T2I diffusion models, where the generated images often do not faithfully represent the semantics of the given text prompts. This issue, known as catastrophic neglect or incorrect modifier binding, can lead to missing objects or improper attribute associations in the generated images, affecting their realism and utility.

🔹 The paper introduces FRAP, an adaptive prompt weighting technique that adjusts the weight coefficients for each token in the text prompt during the RGP. Unlike existing methods that modify the latent code directly and risk generating unrealistic images, FRAP leverages an online optimization algorithm to minimize a unified objective function based on cross-attention maps, strengthening object presence and modifier binding. This approach ensures better semantic alignment without compromising image realism.

🔹 The study shows that FRAP achieves significantly higher prompt-image alignment scores compared to recent methods like Attend & Excite (A&E) and Divide & Bind (D&B) on complex datasets such as COCO-Subject and COCO-Attribute. It also generates more realistic images with lower average latency, reducing inference time by up to 4 seconds compared to D&B.

🔹 The paper concludes that FRAP is effective in generating faithful and realistic images in various challenging scenarios. Future research could focus on integrating FRAP with other prompt optimization techniques, exploring its applicability to other models, and refining its performance on even more complex datasets and scenarios.

📑 Jiang, L., Hassanpour, N., Salameh, M., Singamsetti, M.S., Sun, F., Lu, W., Niu, D. (2024).  FRAP: Faithful and Realistic Text-to-Image Generation with Adaptive Prompt Weighting. DOI: 10.48550/arXiv.2408.11706.