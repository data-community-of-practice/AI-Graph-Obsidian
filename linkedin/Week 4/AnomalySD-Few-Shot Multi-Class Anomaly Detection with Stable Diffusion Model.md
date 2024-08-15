AnomalySD: Revolutionizing Industrial Defect Detection with Few Samples and Many Classes

📌 Industrial anomaly detection faces significant challenges when confronted with limited data and diverse object classes. AnomalySD tackles these issues head-on by leveraging the power of Stable Diffusion models in a novel few-shot, multi-class framework. This approach promises to revolutionize how we detect manufacturing defects, offering a flexible solution that requires minimal normal samples while handling multiple object types with a single model.

Article Link: https://arxiv.org/abs/2408.01960

🔹 Traditional industrial anomaly detection methods often require large datasets of normal samples and separate models for each object type. This approach is impractical in many real-world scenarios where data is scarce due to high labeling costs or privacy concerns. Moreover, the need for multiple specialized models increases computational overhead and reduces flexibility, especially in production lines handling diverse products.

🔹 AnomalySD introduces a groundbreaking approach by adapting Stable Diffusion models for anomaly detection. The method fine-tunes SD on just a few normal samples using carefully designed masks and hierarchical text prompts. During inference, it employs multi-scale and prototype-guided masking strategies to identify potential anomalies. By inpainting these regions and comparing them to the original image, AnomalySD can detect and localize defects across multiple object classes using a single unified model, all while requiring minimal training data.

🔹 The researchers evaluated AnomalySD on two major industrial anomaly detection benchmarks: MVTec-AD and VisA. The results are impressive, especially in few-shot scenarios. With just one normal sample per class, AnomalySD achieved 93.6% image-level AUROC and 94.8% pixel-level AUROC on MVTec-AD, outperforming many existing methods that require more training data. Moreover, AnomalySD demonstrated strong performance in multi-class settings, showcasing its versatility and efficiency in handling diverse object types with a single model.

🔹 The method currently relies on some manual designs, such as crafting text prompts and tuning noise strength. Future research could focus on developing adaptive prompt learning techniques and automated noise guidance to further reduce human intervention. Additionally, exploring how this approach scales to even more diverse and complex industrial scenarios could pave the way for more robust and generalizable anomaly detection systems.

Yan, Z., Fang, Q., Lv, W., & Su, Q. (2024). AnomalySD: Few-Shot Multi-Class Anomaly Detection with Stable Diffusion Model. arXiv. DOI: 10.48550/ARXIV.2408.01960