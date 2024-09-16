Interesting findings from "An Evaluation Framework for Attributed Information Retrieval using Large Language Models"

Article Link : https://arxiv.org/abs/2409.08014

Traditional search engines focus on ranking documents, but with the advent of LLMs, there's a shift towards generating natural language answers. However, LLMs often produce "hallucinations"—statements not supported by their training data. To counter this, attribution methods, which link generated text to source documents, are becoming increasingly important.

Approach : This paper introduces a reproducible evaluation framework that can be used with any LLM to assess attributed information retrieval. It evaluates three architectural designs:

1) Generate (G): Directly generating answers with or without attribution.
2) Retrieve then Generate (RTG): Retrieving relevant documents first, then generating attributed answers.
3) Generate then Retrieve (GTR): Generating answers first, then finding supporting documents.

Key Findings : Using the HAGRID dataset, a benchmark for attributed information-seeking, the paper shows the impact of different approaches on both the correctness and the attributability of the answers. The "Retrieve then Generate" (RTG) approach demonstrated a significant benefit, confirming that retrieving relevant documents before generating answers improves performance. Additionally, the paper highlights the importance of proper attribution and the challenges associated with it.

This framework opens up new avenues for evaluating and improving how LLMs handle information retrieval tasks, with a focus on both the correctness of the information and its attribution. As we move towards more complex information-seeking scenarios, ensuring that LLMs can provide accurate and well-attributed answers will be crucial.

Reference : Djeddal, H., Erbacher, P., Toukal, R., Soulier, L., Katrenko, S., & Tamine, L. (2024). An Evaluation Framework for Attributed Information Retrieval using Large Language Models. _ArXiv_. https://doi.org/10.1145/3627673.3679172
