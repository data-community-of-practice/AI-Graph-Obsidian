KIND: Teaching Diffusion Models to Be Quick Learners

📌 As diffusion models continue to advance in image generation tasks, the challenge of efficiently transferring knowledge to new domains becomes increasingly crucial. Traditional pre-training methods often struggle when faced with significant gaps between training and target tasks. KIND (Knowledge INtegration and Diversion) introduces a novel approach to this problem, reimagining how we condense and transfer knowledge in diffusion models, potentially revolutionizing their adaptability and performance on diverse downstream tasks.

Article Link: https://arxiv.org/abs/2408.07337

🔹 Current pre-training methods for diffusion models prioritize training task performance over knowledge transferability, leading to challenges in adapting to diverse downstream tasks. While Parameter-Efficient Fine-Tuning (PEFT) techniques attempt to address this by adding trainable parameters to fixed pre-trained models, they remain limited by potentially suboptimal pre-trained backbones, hindering effectiveness across varied applications.

🔹 KIND introduces a novel Learngene-based approach for diffusion models, decomposing parameters into "learngenes" for common knowledge and "tailors" for class-specific information. Using SVD-inspired matrix decomposition and a class gate mechanism, KIND shifts pre-training focus from performance to transferable knowledge condensation, creating a more adaptable model for diverse tasks.

🔹 KIND outperformed existing methods in experiments, showing significant improvements in FID and sFID scores on DiT-L/2 models while using fewer parameters and reducing computational costs. It demonstrated faster convergence and better adaptability across various tasks, with its learngenes capturing more generalized knowledge. In some cases, KIND even surpassed full fine-tuning performance.

🔹 KIND significantly advances transfer learning in diffusion models by separating common and class-specific knowledge during pre-training, resulting in more adaptable and efficient models. Future research could explore KIND's application to larger models and diverse tasks, potentially extending to other deep learning domains. This approach may be crucial in developing AI systems that learn quickly from limited data in new domains, as the field progresses towards more efficient and adaptable models.

Xie, Y., Feng, F., Wang, J., Geng, X., & Rui, Y. (2024). KIND: Knowledge Integration and Diversion in Diffusion Models. arXiv. DOI: 10.48550/ARXIV.2408.07337