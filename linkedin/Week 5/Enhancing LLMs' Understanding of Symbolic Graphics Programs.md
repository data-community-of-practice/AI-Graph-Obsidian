Enhancing LLMs' Understanding of Symbolic Graphics Programs

📌 This paper investigates the capability of large language models (LLMs) to understand symbolic graphics programs, a type of computer program used to generate visual content such as 2D images or 3D geometry. The study explores whether LLMs can semantically understand these programs, which involves answering questions about the visual content without directly accessing the rendered images. This problem is significant as it challenges LLMs to demonstrate a form of "visual imagination," making it an important step in evaluating their reasoning abilities in visual contexts.

Article link: https://arxiv.org/abs/2408.08313

🔹 The paper addresses the challenge of assessing the capabilities of LLMs, particularly in understanding symbolic graphics programs, which are programs that can generate visual content like images or 3D models. The task is difficult because it requires the models to answer semantic questions based solely on the symbolic program, without access to the rendered visual content.

🔹 The authors introduce a new benchmark, SGP-Bench, which evaluates the semantic understanding of LLMs regarding symbolic graphics programs. They propose a novel method called Symbolic Instruction Tuning (SIT) to improve LLMs' understanding of these programs. This benchmark and the SIT method provide a scalable way to assess and enhance the visual reasoning capabilities of LLMs, making this study a significant contribution to the field.

🔹 The study finds that existing LLMs struggle with the task of understanding symbolic graphics programs, with performance varying widely among different models. However, models fine-tuned with the SIT method show improved understanding, indicating that this approach can enhance LLMs' capabilities in this area.

🔹 The paper concludes that understanding symbolic graphics programs remains a challenging task for LLMs, but the proposed benchmark and tuning method provide a promising direction for improvement. Future challenges include refining these methods to further enhance LLMs' visual reasoning abilities and exploring other aspects of visual content.

📑 Qiu, Z., Liu, W., Feng, H., Liu, Z., Xiao, Z., Collins, K.M., Tenenbaum, J.B., Weller, A., Black, M.J., Scholkopf, B. (2024).  Can Large Language Models Understand Symbolic Graphics Programs? DOI: 10.48550/arXiv.2408.08313.