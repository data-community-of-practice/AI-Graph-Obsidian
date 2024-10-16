EVOKE and LTI: Battling Overfitting in LLM Knowledge Editing

Article Link: https://arxiv.org/abs/2410.07819

📌 Knowledge editing in Large Language Models (LLMs) has emerged as a promising solution for updating and correcting factual information without retraining. However, this approach faces a significant challenge: Editing Overfit. This phenomenon occurs when edited models disproportionately favor new information, leading to poor performance on complex tasks like multi-hop reasoning. A new study introduces EVOKE, a benchmark for evaluating this issue, and proposes Learn to Inference (LTI), a novel strategy to mitigate overfitting in LLM editing.

🔹 Current LLM knowledge editing methods focus on directly mapping input prompts to edit targets, often using limited samples. This approach can lead to Editing Overfit, where models assign unusually high probabilities to edit targets even in complex scenarios where such responses are implausible. This overfitting hinders the model's ability to generalize new knowledge, particularly in tasks like multi-hop reasoning.

🔹 The researchers introduce EVOKE, a new benchmark for evaluating overfitting in LLM knowledge editing. They also propose Learn to Inference (LTI), a plug-and-play strategy that uses Multi-stage Inference Constraints to guide edited models. LTI aligns the inference process of edited models with that of unedited models using in-context learning, helping prevent overfitting to input-output mappings and improving performance on complex tasks.

🔹 Experiments on EVOKE demonstrate that Editing Overfit is prevalent in current editing methods. The study shows that LTI, when integrated with existing editing techniques like ROME and MEMIT, significantly reduces overfitting. It improves performance on complex tasks such as multi-hop reasoning and prefix distraction, while maintaining high editing efficacy. Notably, LTI outperforms common overfitting mitigation strategies like data augmentation in addressing Editing Overfit.

🔹 This study reveals significant limitations in current LLM knowledge editing approaches and highlights the need for more sophisticated methods of knowledge integration. While LTI shows promise, future research should focus on developing techniques that allow models to recall new knowledge more effectively, mirroring their native knowledge retrieval processes. This could lead to more robust and generalizable knowledge editing in LLMs.

Zhang, M., Ye, X., Liu, Q., Ren, P., Wu, S., & Chen, Z. (2024). Uncovering Overfitting in Large Language Model Editing. arXiv. DOI: 10.48550/ARXIV.2410.07819