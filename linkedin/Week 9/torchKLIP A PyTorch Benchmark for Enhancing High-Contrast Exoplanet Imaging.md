torchKLIP: A PyTorch Benchmark for Enhancing High-Contrast Exoplanet Imaging

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 This paper presents torchKLIP, a PyTorch-based implementation of the Karhunen-Loeve Image Projection (KLIP) algorithm, aimed at improving the post-processing of high-contrast imaging for exoplanet detection. The paper addresses the challenge of distinguishing faint planetary signals from stellar noise, commonly known as speckles. It compares torchKLIP's performance with existing tools, like pyKLIP, and explores its potential for enhancing direct imaging techniques, particularly in exoplanet discovery.

Article link: https://arxiv.org/abs/2409.16466

🔹 The paper highlights the difficulties in detecting exoplanets through direct imaging due to the overwhelming brightness of their host stars, which produces speckle noise that obscures faint planetary signals. Existing post-processing techniques like KLIP are effective but limited, prompting the need for improved methods capable of achieving deeper contrast ratios, particularly for Earth-like planets.

🔹 The study introduces torchKLIP, an innovative implementation of KLIP within the PyTorch machine learning framework. This new tool allows for integration with ML/DL approaches, improving the subtraction of stellar noise and enhancing detection capabilities. TorchKLIP is benchmarked against pyKLIP to assess its performance, showing comparable results in terms of signal-to-noise ratio (SNR) but offering superior computational efficiency, especially in large datasets.

🔹torchKLIP performs comparably to pyKLIP in terms of the SNR for detected exoplanets. However, torchKLIP significantly reduces computation time, making it more efficient and scalable for processing large datasets. The benchmark results demonstrate torchKLIP's potential in advancing exoplanet imaging post-processing, particularly when future instruments with deeper contrast capabilities are deployed.

🔹 The paper concludes that torchKLIP enhances computational efficiency in high-contrast imaging post-processing, with potential for future improvements, including integrating ML and deep learning models. Future work will focus on expanding torchKLIP's capabilities, including applying it to more instruments and observational strategies, and improving contrast ratios for detecting Earth-like exoplanets.

📑 Ko, C.L., Douglas, E.S., Hom, J. (2024).  A PyTorch Benchmark for High-Contrast Imaging Post Processing. DOI: 10.48550/arXiv.2409.16466.