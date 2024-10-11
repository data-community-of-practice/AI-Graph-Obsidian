Advancing Machine Translation with Multi-task Learning: Tackling Emotion-loaded User-generated Content (UGC)

- Link to Article: https://arxiv.org/abs/2410.03277v1.

📍 This study presents a novel multi-task learning (MTL) framework designed to address the unique challenges of translating emotion-laden user-generated content (UGC). The approach improves the quality of machine translation (MT) in handling slang, emotion, and literary devices such as irony and sarcasm—common in social media posts.

🔸 Challenges in MT of Emotion-loaded UGC: Current machine translation systems often fail to preserve emotional subtleties in user-generated content, leading to poor translation of slang, irony, or emotionally charged phrases. Standard metrics struggle to capture this nuance, making it difficult to accurately assess translation quality.

🔸 Capabilities of the Proposed MTL Framework: The MTL framework extends an existing emotion-related dataset by adding sentence-level evaluation scores and word-level emotion labels, allowing for joint training of sentence- and word-level quality estimation (QE) tasks. A new architecture with a combined loss function is introduced, effectively integrating various loss heuristics, including Nash and Aligned losses, to optimize the performance of both tasks.

🔸 Performance and Flexibility: This framework achieves state-of-the-art results in preserving emotional context in translated UGC. Evaluations using multiple datasets demonstrate its ability to handle multiple languages, outperforming existing fine-tuning and MTL methods. The framework is flexible enough to adapt to different data distributions and tasks, making it a valuable tool for evaluating emotion-loaded translations across varied domains.

🔸 Impact and Future Directions: The proposed MTL approach not only advances the quality of emotion-loaded translations but also lays the groundwork for broader applications in translation tasks involving empathy and emotion preservation. Future enhancements aim to validate the model's effectiveness on larger multilingual datasets and investigate its potential in other text processing domains.

🔸 Contribution to Machine Translation: By improving the preservation of emotional context in translations, this framework significantly advances machine translation, particularly in the context of UGC. It contributes to the broader field of natural language processing by addressing the complex task of maintaining emotional integrity in translations.

Reference: Qian, S., Orasan, C., Kanojia, D., & Do Carmo, F. 2024. A Multi-task Learning Framework for Evaluating Machine Translation of Emotion-loaded User-generated Content. arXiv. Available at: https://arxiv.org/abs/2410.03277v1.