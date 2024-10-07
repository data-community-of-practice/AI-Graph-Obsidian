
Interesting findings from "Generative Edge Detection with Stable Diffusion"

Edge detection identifies intensity changes in an image to find object boundaries. It's vital for many downstream tasks, but traditional approaches, even deep learning-based methods, have limitations in balancing precision, robustness, and inference speed. Diffusion models, commonly used for generating images, have recently been explored for edge detection tasks, yet existing models often require lengthy multi-step processes that are computationally expensive.

Novelty: The proposed Generative Edge Detector (GED) takes a new approach by fine-tuning Stable Diffusion, a pre-trained generative model, to predict edge maps directly from latent image features. GED introduces the concept of **granularity**, allowing the model to control the level of detail in the edge maps. By integrating granularity into the U-Net of the diffusion model, GED can produce diverse and fine-grained edge maps without the need for multi-step denoising, making it highly efficient and effective for real-time applications.

Key Findings:
1) GED achieves state-of-the-art performance across multiple datasets (e.g., BSDS500, Multicue, NYUD, and BIPED) with significant improvements in metrics like ODS (Optimal Dataset Scale) and OIS (Optimal Image Scale).
2) The model outperforms previous diffusion-based methods, showing a 3.6% increase in ODS on the BSDS500 dataset and reducing the training steps needed to achieve high performance.
3) GED can generate diverse edge maps with varying levels of detail, offering greater flexibility for different applications.

This work demonstrates that Stable Diffusion, traditionally used for generating images, can be fine-tuned to enhance edge detection tasks. GED’s ability to control edge map granularity makes it a powerful tool for applications requiring detailed boundary detection, from autonomous driving to medical imaging. Its efficiency and versatility position it as a future-ready solution for real-time edge detection.

Reference : Zhou, C., Huang, Y., Xiang, M., Ren, J., Ling, H., & Zhang, J. (2024). Generative Edge Detection with Stable Diffusion. _ArXiv_. https://arxiv.org/abs/2410.03080