Unlearning Trojans in Large Language Models

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 This paper explores the application of Machine Unlearning (MU) techniques to mitigate the impact of trojans embedded in large language models (LLMs). It proposes a novel unlearning approach called Lya, which combines gradient ascent and elastic weight consolidation, a Fisher Information Matrix-based regularization technique. The study compares Lya's effectiveness against conventional techniques like fine-tuning and retraining on models such as BERT and CodeBERT, used for sentiment analysis and code defect detection, respectively.

Article link: https://arxiv.org/abs/2408.12416

🔹 The paper addresses the problem of trojans in LLMs, where adversaries embed malicious behaviors that can be triggered by specific inputs. This is particularly concerning in both natural language models (Text-LLMs) and code models (Code-LLMs), as they can lead to harmful or insecure outputs.

🔹 The paper introduces Lya, a novel approach that integrates gradient ascent with elastic weight consolidation to unlearn trojans from LLMs. This approach is significant because it aims to remove trojan behaviors without the extensive computational costs of retraining from scratch, thus preserving the model's original functionality.

🔹 The study finds that Lya outperforms conventional methods like fine-tuning and retraining in effectively unlearning trojans from poisoned models, demonstrating lower attack success rates while maintaining or improving model accuracy.

🔹 The paper concludes that while Lya shows promise in mitigating trojans in LLMs, further research is needed to explore its application across diverse datasets and models. Future challenges include improving unlearning techniques for code models, which have shown more significant performance degradation compared to natural language models.

📑 Kazemi, M., Hussain, A., Rabin, M.R.I., Alipour, M.A., Lin, Sen. (2024).  Unlearning Trojans in Large Language Models: A Comparison Between Natural Language and Source Code. DOI: 10.48550/arXiv.2408.12416.