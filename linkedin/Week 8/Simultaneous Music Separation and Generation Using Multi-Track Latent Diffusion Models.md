MSG-LD: Unifying Music Generation and Separation in a Single AI Model

📌 Music generation and source separation have traditionally been treated as separate tasks in deep learning, each with its own specialized models. However, the MSG-LD (Music Separation and Generation with Latent Diffusion) approach introduces a unified framework that seamlessly handles both tasks. By learning the joint distribution of interrelated musical tracks, this innovative model bridges the gap between creating new compositions and decomposing existing ones, potentially revolutionizing how we approach music AI.

Article Link: https://arxiv.org/abs/2409.12346

🔹 Traditional approaches to music AI have treated generation and source separation as distinct tasks, requiring separate models and training processes. This division limits the potential for creating versatile music AI systems and fails to capitalize on the inherent relationships between musical elements across different tracks. Existing models often struggle to maintain musical coherence when generating multi-track compositions or separating complex mixtures.

🔹 MSG-LD introduces a unified framework using latent diffusion models to simultaneously handle music generation and source separation. By learning the joint probability distribution of interrelated musical tracks, it can perform three key tasks: source separation, total music generation, and partial track generation (arrangement). The model employs a 3D U-Net architecture to process multiple tracks and uses Classifier-Free Guidance to control the balance between separation and generation modes, offering unprecedented flexibility in music AI applications.

🔹 Experiments on the Slakh2100 dataset demonstrated MSG-LD's superior performance over existing models. In source separation tasks, it significantly outperformed the baseline MSDM model across all instrument tracks. For music generation, MSG-LD reduced the Frechet Audio Distance (FAD) score from 6.55 to 1.30, indicating a substantial improvement in audio quality and musical coherence. The model also excelled in arrangement generation tasks, outperforming MSDM in 13 out of 14 track combinations, showcasing its versatility and effectiveness in handling various musical scenarios.

🔹 MSG-LD marks a significant advance in versatile music AI. Despite current audio quality limitations, future improvements in sampling rates, VAE and vocoder models, and soft conditioning techniques could enhance its capabilities, offering more nuanced control and expanding its applications in music production and creative tools.

Karchkhadze, T.¹, Izadi, M. R., & Dubnov, S. (2024). Simultaneous Music Separation and Generation Using Multi-Track Latent Diffusion Models. arXiv. DOI: 10.48550/ARXIV.2409.12346