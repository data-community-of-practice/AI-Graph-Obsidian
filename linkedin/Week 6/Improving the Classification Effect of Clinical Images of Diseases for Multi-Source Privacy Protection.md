
Interesting findings from "Improving the Classification Effect of Clinical Images of Diseases for Multi-Source Privacy Protection"

Article Link : https://arxiv.org/abs/2408.13038

In the medical field, privacy regulations impede the sharing of sensitive diagnostic data, making it challenging to integrate data from multiple hospitals for accurate model training. Centralized training methods are not suitable due to privacy concerns, and federated learning faces practical issues due to the need for simultaneous participation and the limitations of model parameter averaging. Recent research suggests that linear interpolation in model parameter space can effectively alter model capabilities. Inspired by this, Tian Bowen et al. introduced a framework based on data vectors for medical privacy data, allowing for model fine-tuning on local data and the synthesis of data vectors to improve model performance while maintaining privacy.

**Methodology**  

1. Fine-Tuning Pre-Trained Models: Hospitals fine-tune a unified pre-trained model on local data, updating weights using cross-entropy loss.
2. Calculating Data Vectors: Data vectors are computed as the difference between fine-tuned weights and pre-trained weights, capturing parameter movement directions.
3. Synthetic Total Vector: To address noise and variability, we sum data vectors from multiple hospitals. This aggregated vector is added to the pre-trained weights to generate synthetic weights.
4. Generating and Restoring the Fusion Model: The synthetic weights create a hybrid model combining information from multiple sources. The model is then fine-tuned on a small dataset to restore optimal performance.

Experiments and Results:
Their method was tested on three medical datasets: PAD-UFES-20 (skin disease), Retina (retinal fundus), and Endoscopic Bladder Tissue (bladder tissue). Our data vector-based approach outperformed models trained independently by single hospitals. For instance, on the Endoscopic Bladder Tissue dataset, their method achieved 68.25% accuracy, compared to 60.31% from individual fine-tuning. Random vectors yielded much lower performance, demonstrating the effectiveness of data vectors in optimizing model parameters.

Conclusion:
Data vector-based framework offers a practical solution for training high-performance medical diagnostic models while safeguarding privacy. By integrating model information from multiple hospitals without data exchange or synchronous training, this method advances medical intelligence and provides a new approach to balancing privacy with model training. Future work could explore further optimization of model mixing and its application across various medical domains.

Reference : Bowen, T., Zhengyang, X., Zhihao, Y., Jingying, W., & Yutao, Y. (2024). Improving the Classification Effect of Clinical Images of Diseases for Multi-Source Privacy Protection. _ArXiv_. /abs/2408.13038