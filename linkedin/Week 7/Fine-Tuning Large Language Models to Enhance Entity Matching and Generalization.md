Fine-Tuning Large Language Models to Enhance Entity Matching and Generalization

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 This paper explores the potential of fine-tuning large language models (LLMs) to enhance entity matching tasks, an essential component in data integration pipelines. While previous research emphasized prompt engineering and in-context learning, this study focuses on fine-tuning LLMs to improve performance, particularly regarding generalization across different datasets and domains.

Article link: https://arxiv.org/abs/2409.08185

🔹 Entity matching identifies whether different data descriptions refer to the same entity across various sources. Prior studies showed that LLMs such as GPT and Llama outperform PLMs in zero-shot settings. The goal is to enhance their ability through fine-tuning, addressing issues with cross-domain generalization and in-context learning.

🔹 This study introduces two key dimensions: augmenting training examples with explanations and using LLMs to select or generate better training examples. By fine-tuning smaller and larger models, the research reveals how structured explanations and filtered or generated training examples influence performance. This approach contributes a detailed exploration of the potential for fine-tuning to go beyond prompt engineering, particularly in improving generalization within and across domains.

🔹 Fine-tuning leads to notable improvements in smaller models and enhances in-domain generalization. The addition of structured explanations boosts performance across three of four models. However, fine-tuning’s effect on larger models, such as GPT-4o, remains mixed, and cross-domain generalization often suffers.

🔹 Fine-tuning enhances smaller models' performance, especially in specific domains, but struggles to improve cross-domain capabilities. Future research should focus on refining example generation methods to address these cross-domain limitations and improve the generalization capabilities of LLMs.

📑 Steiner, A., Peeters, R., Bizer, C. (2024).  Fine-tuning Large Language Models for Entity Matching. DOI: 10.48550/arXiv.2409.08185.