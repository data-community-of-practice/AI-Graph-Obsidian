Zijian Yang

ORCiD: 0009-0006-8301-7634

------

Boosting Image Classification with Graph Neural Networks and Manifold Learning

Article link: https://arxiv.org/abs/2409.13063

📌This research explores the untapped potential of Graph Neural Networks (GNNs) in image classification by integrating manifold learning. The study applies the manifold hypothesis to reduce the dimensionality of image data, preserving its geometric structure while enhancing classification accuracy.

🔹Image classification has traditionally relied on convolutional neural networks, but high-dimensional data poses challenges for these methods. This study adopts a novel approach by representing images as nodes in a graph, utilizing manifold learning to build low-dimensional image representations. The integration of variational autoencoders (VAEs) aids in capturing these representations efficiently.

🔹The innovation lies in constructing a graph where each node represents an image and its connections reflect the geometric relationships between image embeddings. By applying GNNs to this structure, the research demonstrates a more effective generalization to unseen data, outperforming traditional multilayer perceptron models in tasks like MNIST and CIFAR10 classification.

🔹The results are significant, showing GNNs trained on this manifold representation achieving better accuracy and generalization across both small and large datasets. The method reduces the gap between training and test accuracy, particularly with increasing node samples, proving its robustness in real-world applications.

🔹The implications of this study extend beyond image classification. The proposed framework opens up new possibilities for deep learning in domains where data lacks explicit geometric structure, making it a promising tool for various AI applications. Future work may explore scaling this approach to more complex datasets and further refining its efficiency.

Netto, Wang, Z., & Ruiz, L. (2024). Improved Image Classification with Manifold Neural Networks. [ArXiv.org](http://ArXiv.org). https://arxiv.org/abs/2409.13063