## Instruct Large Language Models to Generate Scientific Literature Survey Step by Step


**Abstract:** The paper presents a novel methodology for automating the generation of scientific literature surveys using Large Language Models (LLMs). The research addresses the growing challenge of conducting comprehensive literature reviews in the face of an ever-expanding body of scientific publications. By systematically leveraging LLMs to generate titles, abstracts, hierarchical headings, and main content in a sequential manner, the authors have significantly improved the coherence and relevance of generated surveys. 

**Link:** [arXiv:2408.07884v1](https://arxiv.org/abs/2408.07884v1)

1️⃣ **Problem & Context:** The exponential growth of scientific publications poses a significant challenge for researchers, who must dedicate substantial time to conducting literature reviews. This paper tackles the problem by introducing a step-by-step approach to literature survey generation using LLMs.

2️⃣ **Methodology & Contribution:** The authors designed a series of prompts that guide LLMs to generate literature surveys in stages—beginning with the title and abstract, followed by the hierarchical structure, and concluding with the detailed content. This approach ensures that the LLM maintains a high-level perspective throughout the process, thereby improving the logical flow and reducing the costs associated with API usage.

3️⃣ **Key Findings:** The implementation of this method using Alibaba’s Qwen-long model achieved third place in the NLPCC 2024 Scientific Literature Survey Generation evaluation task, with a minimal margin behind the second-place team. The model demonstrated an impressive soft heading recall of 95.84%, underscoring the effectiveness of the sequential generation design.

4️⃣ **Conclusion & Future Challenges:** While the proposed method significantly enhances the quality and efficiency of automated literature surveys, challenges remain in ensuring the accuracy of citations and mitigating the hallucination effects of LLMs. Future work will focus on integrating reference content to improve factual reliability, aiming to develop a more robust and trustworthy system for automatic literature survey generation.

**Reference:** Lai, Y., Wu, Y., Wang, Y., Hu, W., & Zheng, C. (2024). "Instruct Large Language Models to Generate Scientific Literature Survey Step by Step. ArXiv." /abs/2408.07884
