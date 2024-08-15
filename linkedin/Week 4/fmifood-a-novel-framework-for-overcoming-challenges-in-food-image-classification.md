FMiFood: A Novel Framework for Overcoming Challenges in Food Image Classification

📌 This paper discusses a novel approach to food image classification, a crucial step in image-based dietary assessment. The goal of this assessment is to estimate nutrient intake from images of eating occasions, which is vital for applications in nutrition science and healthcare. However, the task is challenging due to intra-class diversity (variations within the same food category) and inter-class similarity (similarities between different food categories), which often lead to misclassification and reduced accuracy.

Article link: https://arxiv.org/abs/2408.03922

🔹 The primary challenge addressed by the paper is the difficulty in accurately classifying food images due to the high degree of similarity between different food categories (inter-class similarity) and the variations within the same category (intra-class diversity). These challenges make it hard for traditional image classification models to perform well, thereby limiting the effectiveness of dietary assessments based on image data.

🔹 The paper introduces **FMiFood**, a new framework for food image classification using multi-modal contrastive learning. Its key innovation is the **flexible matching technique**, allowing image patches to match multiple or no text tokens, leading to a more nuanced understanding of images. Additionally, GPT-4 generates detailed text descriptions, enhancing the model's ability to distinguish visually similar food items. This approach improves classification accuracy and offers a new method for integrating contextual information into image classification.

🔹 The FMiFood model was tested on two datasets, UPMC-Food101 and VFN, where it outperformed existing models. It effectively addressed intra-class diversity and inter-class similarity, resulting in more accurate food image classification. The flexible matching technique and GPT-4 generated text descriptions were key in enhancing performance, leading to the highest average classification accuracy among state-of-the-art methods.

🔹 The paper concludes that FMiFood significantly advances food image classification by effectively addressing intra-class diversity and inter-class similarity. The use of multi-modal data and enriched contextual information has proven effective in improving accuracy. The authors suggest future work should focus on refining the flexible matching technique to filter out irrelevant information, further enhancing the model’s robustness.

📑 Pan, X., He, J., Zhu, F. (2024).  FMiFood: Multi-modal Contrastive Learning for Food Image Classification. DOI: 10.48550/arXiv.2408.03922.