# Enhancing Trustworthiness in Large Language Models Through Knowledge Graph Integration

## Introduction
This paper investigates how integrating Knowledge Graphs (KGs) with Large Language Models (LLMs) can mitigate issues of hallucination—where models generate factually incorrect information—particularly in complex, open-ended question-answering tasks. To address the gap in current benchmarks that focus primarily on closed-ended tasks, the authors propose a novel benchmark called **OKGQA**. Additionally, **OKGQA-P** is introduced to test the robustness of LLM+KG systems when exposed to contaminated or perturbed KGs.

**Article link:** https://arxiv.org/abs/2410.08085


## 1️⃣ Problem Statement
LLMs have shown a significant ability to generate human-like responses but are still prone to hallucinations due to knowledge gaps, especially when tasked with open-ended, real-world questions. This issue is exacerbated in applications where factual precision is critical, such as scientific inquiry and healthcare. Current benchmarks primarily assess LLMs in closed-ended tasks, leaving their performance in complex, open-ended scenarios underexplored.

## 2️⃣ Methodology
The paper introduces **OKGQA**, a benchmark designed to assess LLMs augmented with Knowledge Graphs in open-ended question-answering tasks. The framework focuses on real-world applications, incorporating diverse types of questions such as descriptive, explanatory, and predictive queries. OKGQA also includes metrics to evaluate both the reduction in hallucinations and the enhancement of reasoning capabilities. Moreover, the paper presents **OKGQA-P**, a variant designed to evaluate model performance under conditions where KGs are deliberately perturbed with incorrect or incomplete information. This approach allows the authors to examine the resilience of LLMs to noise in KGs.

## 3️⃣ Key Findings
- LLMs integrated with KGs show significant improvements in factual accuracy, reducing hallucination rates in open-ended QA tasks, particularly in reasoning-heavy queries.
- Subgraph-based retrieval methods outperform other KG integration techniques (e.g., triplet or path retrieval) by providing more robust performance across various types of queries.
- Even when the KGs are contaminated, the integration of KGs still reduces hallucination rates, demonstrating the resilience of the combined system.
- Internal reasoning strategies (e.g., Chain-of-Thought, self-consistency) improve response quality but are less effective at reducing hallucinations than external KG integration.

## 4️⃣ Final Conclusion and Future Challenges
The study demonstrates that integrating KGs with LLMs can effectively reduce hallucinations in open-ended question-answering, even when the KGs contain errors. However, challenges remain in improving the robustness and quality of KGs, especially when dealing with noisy or incomplete data. Future research should focus on optimizing retrieval methods and KG quality, as well as exploring the limits of KG augmentation in even more complex, real-world scenarios.

## Reference
Sui, Y., Hooi, B., 2024, "Can Knowledge Graphs Make Large Language Models More Trustworthy? An Empirical Study Over Open-Ended Question Answering," arXiv:2410.08085.

