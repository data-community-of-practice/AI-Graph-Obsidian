ONE2SET + LLM: A Powerful Duo for Smarter Keyphrase Generation

📌 Keyphrase generation (KPG) is a crucial task in natural language processing, but existing models struggle to balance precision and recall effectively. This paper introduces a novel "generate-then-select" framework that combines the strengths of a ONE2SET-based generator with a large language model (LLM) selector. By addressing the precision-recall trade-off, this approach significantly improves keyphrase generation performance, especially for absent keyphrases not explicitly present in the text.

Article Link: https://arxiv.org/abs/2410.03421

🔹 Existing KPG models face a trade-off between precision and recall. Models that excel in recall tend to generate more incorrect keyphrases, while those with high precision often miss important concepts. This makes it challenging for a single model to achieve high performance in both metrics simultaneously, limiting the overall effectiveness of KPG systems.

🔹 The paper introduces a novel "generate-then-select" framework that combines a ONE2SET-based generator with a large language model (LLM) selector. The generator uses an Optimal Transport (OT) based assignment strategy to improve keyphrase recall, while the selector employs a sequence labeling approach to enhance precision and reduce semantic repetition. This two-step process effectively addresses the precision-recall trade-off, significantly improving overall KPG performance.

🔹 Experimental results across multiple benchmark datasets show that this framework significantly outperforms state-of-the-art models, especially in absent keyphrase prediction. The approach demonstrates robust performance across different LLMs, including LLaMA-2-7B and Zephyr-7B. Notably, the method achieves higher F1 scores for both present and absent keyphrases compared to existing techniques, with particularly substantial improvements in generating absent keyphrases.

🔹 While this framework significantly advances KPG performance, it comes with increased computational demands due to the use of large language models. Future work could focus on optimizing the framework for efficiency, exploring its applicability to domain-specific KPG tasks, and investigating how to further improve the generation of absent keyphrases. The success of this approach also opens up possibilities for similar two-stage frameworks in other natural language processing tasks.

Shao, L., Zhang, L., Peng, M., Ma, G., Yue, H., Sun, M., & Su, J. (2024). ONE2SET + Large Language Model: Best Partners for Keyphrase Generation. arXiv. DOI: 10.48550/ARXIV.2410.03421