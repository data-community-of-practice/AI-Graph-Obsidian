## Instruct Large Language Models to Generate Scientific Literature Survey Step by Step

### Introduction
Automating the generation of scientific literature surveys presents a complex challenge that demands a deep understanding of both subject matter and the ability to systematically organize and present information. Leveraging Large Language Models (LLMs) for this task has shown promising potential. This article deep dives into the innovative approach for harnessing LLMs to produce high-quality literature surveys, which earned us a commendable third place in the NLPCC 2024 Scientific Literature Survey Generation evaluation.

**Article Link** : https://arxiv.org/abs/2408.07884

### Methodology

- **Sequential Generation Framework:** We adopted a stepwise instruction paradigm, prioritizing the generation of titles and headings before progressing to content creation. This structured methodology facilitates a coherent and hierarchical presentation of information.

- **Text Embedding with BGE-Large-En-V1.56:** We utilized the BGE-Large-En-V1.56 model for embedding text, which is critical for assessing semantic similarity between generated and reference surveys. This model ensures that the generated headings are both contextually relevant and distinct.

- **Soft Heading Recall Metric:** We introduced the soft heading recall metric to evaluate the overlap between generated and reference headings. Our system achieved a notable 95.84% in soft heading recall, securing a second-place position in this metric.

- **Human Evaluation Criteria:** In addition to automated metrics, we conducted human evaluations to assess several qualitative aspects:
  - **Linguistic Fluency:** Clarity and readability of the generated text.
  - **Structural Coherence:** Logical organization and flow of the content.
  - **Citation Integrity:** Accuracy and reliability of references.
  - **Content Relevance:** Adherence to the thematic focus of the survey.
  - **Analytical Depth:** Breadth and depth of the analytical coverage.

### Key Findings
Our results were highly competitive and insightful:

- **Overall Performance:** We ranked third, with an overall score just 0.03% below the second-place team.
  
- **Heading Generation Performance:** The sequential generation design significantly improved heading generation, as evidenced by our high soft heading recall score.

- **Challenges in Human Evaluation:** While automated metrics were robust, human evaluations identified challenges related to citation accuracy and the occurrence of hallucinations—instances where the LLM generates plausible but incorrect or unverifiable content.

### Conclusion
Our research demonstrates the potential of LLMs in automating the generation of scientific literature surveys. By implementing a structured, sequential generation framework, we achieved high performance in the NLPCC 2024 evaluation. Nonetheless, challenges such as ensuring citation accuracy and mitigating hallucinations persist. Future work will focus on integrating reference content to enhance the factual accuracy and reliability of generated surveys and refining the generation framework for more precise outputs. Future improvements will include deeper integration of reference content to address factual inaccuracies and enhance citation reliability. Additionally, we plan to optimize the sequential generation framework to produce more concise and targeted outlines.

**References**: 
- Lai, Y., Wu, Y., Wang, Y., Hu, W., & Zheng, C., 2024, "Instruct Large Language Models to Generate Scientific Literature Survey Step by Step." ArXiv. /abs/2408.07884

