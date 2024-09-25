# CLAIRA - Leveraging Large Language Models to Judge Audio Captions

In this latest research, CLAIRA introduces a novel and flexible method for evaluating machine-generated audio captions. The study addresses a critical need for accurate and transparent evaluation in Automated Audio Captioning (AAC), offering a solution that leverages large language models (LLMs) to score and interpret audio descriptions. 

**Article link:** https://arxiv.org/pdf/2409.12962

## 1️⃣ The Challenge
Traditional metrics like BLEU and ROUGE often fall short in capturing the nuanced semantic relationships between audio captions and human-written references, resulting in less accurate evaluations.

## 2️⃣ Introducing CLAIRA
CLAIRA uses the zero-shot capabilities of LLMs to directly assess the semantic distance between captions and references, providing not only a numeric score but also detailed justifications for its evaluations. This approach simplifies the evaluation process while improving alignment with human judgment.

## 3️⃣ Key Findings
- CLAIRA demonstrates up to 11% improvement in accuracy over other metrics on the Clotho-Eval dataset.
- It produces more interpretable evaluations, with its explanations rated up to 30% better by human evaluators, showcasing the method's transparency and precision.

## 4️⃣ Future Outlook
While CLAIRA represents a significant advancement, challenges remain in further refining the method for multilingual datasets and exploring its applicability across broader audio domains. The next steps will likely involve enhancing the robustness of the approach to handle more diverse soundscapes and languages.

### Reference
Wu, T-H., Gonzalez, J.E., Darrell, T., Chan, D.M., 2024, CLAIRA: Leveraging Large Language Models to Judge Audio Captions, IEEE International Conference on Audio Processing. arXiv:2409.12962. 
