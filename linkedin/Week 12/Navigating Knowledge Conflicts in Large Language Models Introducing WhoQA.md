Zijian Yang

ORCiD: 0009-0006-8301-7634

------

Navigating Knowledge Conflicts in Large Language Models: Introducing WhoQA

**Article link:** https://arxiv.org/abs/2410.15737

📌Understanding and addressing knowledge conflicts in large language models (LLMs) is crucial, especially in real-world applications where multiple, conflicting sources of information are common. This research delves into how LLMs handle these conflicts, proposing solutions for more transparent and accurate responses.

🔹The rise of retrieval-augmented generation (RAG) methods has been a game-changer in supplementing the static memory of pre-trained models with real-time data. However, these models often face challenges when conflicting information is retrieved, leading to biased or incomplete responses. The WhoQA dataset was introduced to benchmark how LLMs manage such knowledge conflicts, offering valuable insights into their behavior.

🔹WhoQA presents a novel framework that induces conflicts by asking questions about entities with the same name but different attributes. By compiling over 5,000 questions from Wikipedia and Wikidata, this dataset tests models’ ability to provide accurate, multi-answer responses, addressing conflicts directly rather than prioritizing more popular or prominent information.

🔹The findings reveal that knowledge conflicts significantly impair the performance of even the most advanced LLMs, highlighting the models' tendency to overlook subtle conflicts. For instance, when asked about George Washington’s occupation, LLMs often prioritize the U.S. president, neglecting lesser-known individuals with the same name.

🔹WhoQA’s results underline the need for more sophisticated approaches to handling knowledge conflicts in LLMs. By fostering greater transparency and enabling users to make informed decisions, this benchmark paves the way for future research in improving model accuracy and reducing biases, especially in high-stakes applications.

Pham, Q. H., Ngo, H., Luu, A. T., & Nguyen, D. Q. (2024). Who’s Who: Large Language Models Meet Knowledge Conflicts in Practice. [ArXiv.org](http://ArXiv.org). https://arxiv.org/abs/2410.15737