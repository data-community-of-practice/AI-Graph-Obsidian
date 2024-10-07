Multi-Audio ALLMs: Expanding the Sonic Horizons of AI

📌 Audio Large Language Models (ALLMs) have made significant strides in processing single audio inputs, but real-world applications often require handling multiple audio streams simultaneously. This paper introduces the first dedicated multi-audio benchmark and a novel multi-audio large language model (MALLM), addressing a critical gap in the field of audio AI. By advancing multi-audio processing capabilities, this research brings us closer to replicating human-like auditory abilities in machines, potentially revolutionizing applications like virtual assistants and human-computer interaction.

Article Link: https://arxiv.org/abs/2409.18680

🔹 Current ALLMs excel at processing single audio inputs but struggle with multi-audio scenarios. This limitation hinders their applicability in real-world situations where processing multiple audio streams simultaneously is crucial. Unlike text and vision domains, the audio field lacks systematic evaluations and benchmarks for multi-audio tasks, creating a significant gap in ALLM development and assessment.

🔹 This paper introduces two major contributions: (1) The first multi-audio evaluation (MAE) benchmark, comprising 20 datasets across 11 multi-audio tasks in both speech and sound domains. (2) A novel multi-audio large language model (MALLM) that uses discriminative learning on synthetic data to effectively capture audio contexts. This innovative approach enables multi-audio processing without the need for extensive data collection or human labeling, marking a significant advancement in ALLM capabilities.

🔹 Comprehensive experiments on the MAE benchmark reveal that existing open-source ALLMs struggle with multi-audio tasks despite their strong single-audio capabilities. The proposed MALLM significantly outperforms all baselines, achieving an average accuracy of 73.8% on speech tasks and 74.1% on sound tasks. Notably, MALLM maintains competitive performance on single-audio tasks while demonstrating superior multi-audio processing abilities, bridging the gap between open-source and proprietary models in some areas.

🔹 This work lays a robust foundation for future research in multi-audio processing for ALLMs. While the current benchmark may be too simple for advanced proprietary models, it opens doors for more complex multi-audio tasks. Future challenges include extending the benchmark to multilingual scenarios, scaling up the MALLM training data, and applying these techniques to more challenging domains like singing and music processing.

Chen, Y., Yue, X., Gao, X., Zhang, C., D'Haro, L. F., Tan, R. T., & Li, H. (2024). Beyond Single-Audio: Advancing Multi-Audio Processing in Audio Large Language Models. arXiv. DOI: 10.48550/ARXIV.2409.18680