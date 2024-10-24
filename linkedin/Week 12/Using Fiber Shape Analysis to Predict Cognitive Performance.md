# Using Fiber Shape Analysis to Predict Cognitive Performance

**Introduction:**  
The paper, *The Shape of the Brain’s Connections is Predictive of Cognitive Performance: An Explainable Deep Learning Study*, investigates the predictive power of white matter fiber shape features on cognitive performance. Leveraging diffusion MRI (dMRI) tractography, the study introduces shape-based features and applies machine learning to analyze cognitive assessment data from the Human Connectome Project.

**Article link:** https://arxiv.org/abs/2410.15108

1️⃣ **Understanding the Problem**: Traditional metrics in dMRI tractography, like the number of streamlines (NoS), fractional anisotropy (FA), and mean diffusivity (MD), primarily focus on microstructure and connectivity. However, these measures fail to capture comprehensive morphometric details, such as the volume, surface area, and geometric irregularity of brain connections. This oversight limits the understanding of how these structural variations impact individual cognitive functions.

2️⃣ **New Methodology**: The authors employed an explainable machine learning pipeline, integrating a one-dimensional convolutional neural network (1D-CNN) with SHAP (SHapley Additive exPlanations) analysis to predict cognitive scores based on shape, connectivity, and microstructure features. They analyzed a total of 12 shape features, including diameter, elongation, and trunk volume, across 953 fiber clusters segmented from whole-brain tractography. The study compared the predictive performance of these shape features with traditional measures using seven NIH Toolbox cognitive assessments.

3️⃣ **Key Findings**: Shape descriptors, particularly irregularity, exhibited prediction performance on par with or superior to traditional connectivity and microstructure metrics. For instance, the irregularity measure consistently outperformed NoS and FA in predicting cognitive scores across multiple assessments, such as the Picture Vocabulary Test (TPVT) and the Dimensional Change Card Sort Test (TCST). The explainable AI module further highlighted highly predictive fiber clusters within deep association pathways, cerebellar regions, and projection tracts, emphasizing their distributed relevance across cognitive domains.

4️⃣ **Conclusion and Next Steps**: This study successfully demonstrates that white matter shape features, like fiber cluster diameter and surface irregularity, are crucial predictors of cognitive performance. These findings challenge conventional paradigms that prioritize connectivity-based metrics, suggesting a paradigm shift toward incorporating shape analysis in neuroimaging studies. Future research could explore multi-view learning techniques to integrate shape, microstructure, and connectivity features and extend validation to diverse cohorts and neuropathological datasets.

**Reference**: Yui Lo, Yuqian Chen, Dongnan Liu, Wan Liu, Leo Zekelman, Jarrett Rushmore, Fan Zhang, Yogesh Rathi, Nikos Makris, Alexandra J. Golby, Weidong Cai, Lauren J. O’Donnell, 2024, *The Shape of the Brain’s Connections is Predictive of Cognitive Performance: An Explainable Deep Learning Study*, DOI: 10.48550/arXiv.2410.15108

