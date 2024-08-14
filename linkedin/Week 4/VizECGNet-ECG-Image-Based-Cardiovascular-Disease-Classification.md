VizECGNet: ECG Image-Based Cardiovascular Disease Classification

📌 This paper introduces VizECGNet, a novel deep learning model designed for the classification of cardiovascular diseases using ECG images. The study addresses a significant challenge in clinical settings where digitized ECG signals are often unavailable, particularly in smaller clinics due to high maintenance costs or the use of legacy devices. By leveraging only printed ECG graphics, VizECGNet provides a solution for predicting multiple cardiovascular diseases, offering a practical approach in environments where traditional signal-based ECG analysis is not feasible.

Article link: https://arxiv.org/abs/2408.02888

🔹 The paper addresses the challenge of diagnosing cardiovascular diseases in settings where digitized ECG signals are unavailable. Many smaller clinics store ECG data as printed images due to cost constraints, limiting the use of deep learning models that require digital signals. This study proposes a model that works with printed ECG images, bridging this gap.

🔹 The novelty of this study lies in the introduction of VizECGNet, a multi-modal deep learning framework that combines image-based and signal-based modalities through cross-modal attention modules (CMAM) and self-modal attention modules (SMAM), both of which enhance feature extraction. The model integrates features during training but uniquely allows for disease classification using only ECG images during inference. Additionally, knowledge distillation is employed to maintain high accuracy, making advanced classification techniques accessible in environments where only ECG images are available.

🔹 The key findings show that VizECGNet outperforms existing signal- and image-based ECG classification models in precision, recall, and F1-Score, with improvements of 3.50%, 8.21%, and 7.38% over traditional signal-based models. Additionally, when using only printed ECG images, VizECGNet achieves up to 24.06% higher F1-Score than other image-based models, demonstrating its robustness and practical value in clinical settings.

🔹 In conclusion, VizECGNet provides a robust solution for classifying cardiovascular diseases using printed ECG images, making it ideal for resource-limited settings. The study highlights the model’s potential in developing countries. Future work includes enhancing its generalization by training on diverse 12-lead ECG datasets and testing in real clinical settings, with the possibility of developing it into a practical application for broader use.

📑 Nam, J.H., Park, S.H., Kim, S.J., Lee, S.C. (2024).  VizECGNet: Visual ECG Image Network for Cardiovascular Diseases Classification with Multi-Modal Training and Knowledge Distillation. DOI: 10.48550/arXiv.2408.02888.