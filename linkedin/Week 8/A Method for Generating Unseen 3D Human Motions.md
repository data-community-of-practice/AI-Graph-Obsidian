A Method for Generating Unseen 3D Human Motions

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 This paper presents a novel approach to generating realistic 3D human motions for action classes not seen during training. By decomposing complex actions into simpler, known sub-movements using GPT models, and then recombining them with diffusion models, the method generates coherent animations without requiring additional training data. This technique advances motion generation, particularly for applications like video games and animation, where intuitive and flexible methods are essential.

Article link: https://arxiv.org/abs/2409.11920

🔹 The paper tackles the issue of generating realistic 3D human motions for actions not included in the training set. Existing methods rely on collecting new motion data, which is inefficient and costly. The approach addresses the need for a solution that generates unseen motions without retraining models, which is crucial in areas like gaming and film.

🔹 The Motion Composition Diffusion (MCD) framework breaks down complex motions into simple movements using GPT and then recombines them with diffusion models to generate unseen actions. This method enables both temporal and spatial composition of movements and can be integrated with any pre-trained diffusion model, offering flexibility and broader application.

🔹MCD successfully generates complex motions by decomposing and recombining known movements, outperforming existing text-conditioned models. It achieves better alignment with ground truth and smoother transitions, resulting in more realistic animations, validated through tests on benchmark datasets.

🔹 MCD is a promising solution for generating unseen motions. Future improvements could focus on enhancing GPT’s decomposition abilities and expanding the diversity of training data to improve the system’s ability to handle more complex or overlapping actions​

📑 Mandelli, L., Berretti, S. (2024).  Generation of Complex 3D Human Motion by Temporal and Spatial Composition of Diffusion Models. DOI: 10.48550/arXiv.2409.11920.