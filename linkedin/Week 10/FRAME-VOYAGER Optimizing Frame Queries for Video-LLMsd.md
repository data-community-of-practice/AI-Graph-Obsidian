FRAME-VOYAGER: Optimizing Frame Queries for Video-LLMs

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 The paper addresses the limitations of existing Video-Large Language Models (Video-LLMs), particularly their inability to process entire videos due to input token length constraints. It introduces a novel framework called FRAME-VOYAGER, which queries informative frame combinations based on textual queries in video tasks. The key contribution of the paper is the development of an automated data collection and labeling pipeline, using a pre-trained Video-LLM to rank frame combinations by prediction loss. This ranking supervises FRAME-VOYAGER to select the optimal frame combinations.

Article link: https://arxiv.org/abs/2410.03226

🔹 Current methods such as uniform sampling and text-frame retrieval fail to capture the complexity of videos with varying information density and complex instructions. The inability to input entire videos into models due to token length constraints limits the performance of Video-LLMs.

🔹 FRAME-VOYAGER proposes an innovative frame-querying approach that learns to select optimal frame combinations for better video understanding. The ranking of frame combinations is based on prediction losses from a pre-trained Video-LLM, providing a supervised learning signal. This allows the framework to overcome the limitations of traditional methods and improve the performance of video models without significantly increasing computational complexity.

🔹FRAME-VOYAGER, when evaluated on four Video Question Answering benchmarks, showed significant improvements over baseline methods, especially in tasks requiring reasoning and information synopsis in long videos. The results demonstrated that the model could be a plug-and-play solution for Video-LLMs, enhancing their ability to process and understand videos.

🔹 The paper concludes that FRAME-VOYAGER effectively addresses the challenges of frame selection in video tasks and enhances video model performance. However, future work could focus on integrating this approach into the pre-training of Video-LLMs and exploring its application to longer videos.

📑 Yu, S., Jin, C., Wang, H., Chen, Z., Jin, S., Zuo, Z., Xu, X., Sun, Z., Zhang, B., Wu, J., Zhang, H., Sun, Q. (2024). Frame-Voyager: Learning to Query Frames for Video Large Language Models. DOI: 10.48550/arXiv.2410.03226.