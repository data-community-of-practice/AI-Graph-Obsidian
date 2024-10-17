
Interesting findings from "Generated Bias: Auditing Internal Bias Dynamics of Text-To-Image Generative Models"

Text-to-image (TTI) models like Stable Diffusion and DALL-E are transforming the way we create visual content from text descriptions. However, they come with challenges, particularly when it comes to gender bias. This paper explores the bias that occurs in the internal processes of TTI models, offering new metrics to measure how much bias is introduced and amplified during the image generation process.

The authors propose two key metrics:

1. Diffusion Bias, which measures the bias introduced by the diffusion process itself.
2. Bias Amplification, which quantifies how much the bias increases when converting text into an image.

Key Findings:

1)  The study reveals that both DALL-E 2 and Stable Diffusion v2 amplify gender stereotypes, with Stable Diffusion showing higher bias levels.
2)  These models are more likely to generate male images for traditionally male-dominated professions (e.g., engineer, CEO) and female images for professions historically dominated by women (e.g., nurse, librarian).
3)  Bias is not just present at the output level but is introduced and amplified internally throughout the multi-stage process of generating images from text prompts.

As the use of TTI models grows, understanding and addressing bias within their internal architecture is critical. The proposed metrics, Diffusion Bias and Bias Amplification, provide new ways to measure and potentially mitigate these issues. By doing so, we can create more inclusive and fair AI systems.

Article Link : https://arxiv.org/abs/2410.07884

Reference : Mandal, A., Leavy, S., & Little, S. (2024). Generated Bias: Auditing Internal Bias Dynamics of Text-To-Image Generative Models. _ArXiv_. https://arxiv.org/abs/2410.07884

