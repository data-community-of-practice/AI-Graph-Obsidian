Relightable 3D Car Asset Generation from Single Images

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 The paper introduces a novel framework for generating high-quality 3D car assets from a single image. This paper addresses the limitations of current methods that generate non-relightable 3D objects, limiting their utility under different lighting conditions, which is crucial for applications in video games, autonomous driving, and virtual reality.

Article link: https://arxiv.org/abs/2410.08181

🔹 The paper focuses on the challenge of generating photorealistic 3D car assets that can be relighted under various lighting conditions. Traditional 3D generation methods lack the capability to model material properties such as roughness and metallic, limiting their applicability in real-world tasks.

🔹The authors propose a relightable 3D Gaussian splatting (3D-GS) generative model (RGM) that reconstructs 3D car geometry, textures, and material properties from a single input image. The model integrates a large synthetic car dataset with over 1,000 high-precision models, offering significant improvements over existing methods. This enables the generation of 3D car assets that can be seamlessly relighted in different environments.

🔹Experimental results demonstrate that RGM outperforms existing methods in generating high-fidelity 3D car models. It achieves superior performance in rendering material properties and enabling realistic relighting. The generated 3D assets can be effectively used in road scenes for autonomous driving simulation and other industrial applications.

🔹 The paper concludes by highlighting the significance of relightable 3D object generation and its implications for industrial applications. Future challenges include further optimizing the model's efficiency and extending its applicability to more complex 3D scenes, such as those involving dynamic lighting and multi-object interactions​

📑 Chen, X., Zheng, J., Huang, H., Xu, H., Gu, W., Chen, K., Xiang, H., Gao, H.A., Zhao, H., Zhou, G., Zhang, Y. (2024). RGM: Reconstructing High-fidelity 3D Car Assets with Relightable 3D-GS Generative Model from a Single Image. DOI: 10.48550/arXiv.2410.08181.