Where to Build Food Banks and Pantries: A Two-Level Machine Learning Approach  
Link to Article: https://arxiv.org/abs/2410.15420

📍 Overview: This study presents a novel two-level machine learning framework to optimize the locations of food banks and pantries, aiming to reduce travel distances for food-insecure families. Using K-Medoids clustering and the Open-Source Routing Machine (OSRM), this framework models real driving distances, offering a practical approach to improve food access.

🔸 Challenges of Location Optimization: Food banks and pantries often lack optimal placement, with many underserved communities. This research tackles the logistical challenge by calculating realistic travel routes and distances, rather than relying solely on Euclidean measurements, for better accessibility.

🔸 Capabilities of the Two-Level Model: This approach involves two layers:

- Food Bank Clustering: K-Medoids is first used to find ideal food bank locations across larger geographic areas.
- Pantry Clustering: Within each food bank’s region, K-Medoids refines pantry locations, prioritizing proximity to high-need areas.

🔸 Performance and Flexibility: When applied in California and Indiana, this framework reduced the household-to-pantry travel distance by an average of 5.72 miles in California and 3.52 miles in Indiana. Though food bank-to-pantry distances slightly increased, household savings outweighed this penalty, making the model a viable tool for agencies nationwide.

🔸 Impact and Future Directions: This framework not only supports strategic planning for current food bank systems but also offers potential applications in areas with limited food assistance infrastructure. Future improvements will consider factors like food bank capacity for even more practical implementation.

🔸 Contribution to Community Support Systems: By optimizing location accessibility, this model enhances food security initiatives, providing a powerful tool for organizations aiming to make food aid more reachable to those in need.

Reference: Ruan, G., Guo, Z., Lin, G., 2024. Where to Build Food Banks and Pantries: A Two-Level Machine Learning Approach. arXiv:2410.15420v1. Available at: https://arxiv.org/abs/2410.15420