# _Challenging Conventional AI: The Limitations of Image Processing in Duplicate Question Detection_
- Aditya Iyengar (ORCID: 0009-0005-1959-9724)
- Link to Article: [arxiv.org/abs/2407.05523](https://arxiv.org/abs/2407.05523)

📍 The research article "Negative Results of Image Processing for Identifying Duplicate Questions on Stack Overflow" scrutinises the efficacy of integrating image processing with traditional text-based methods for detecting duplicate questions on Stack Overflow. Despite innovative approaches, the enhancement in accuracy was marginal.

🔸 *Study Insights*: The study employed OCR to extract textual content from images and automated image captioning to interpret visual data. For instance, consider a scenario where two different questions on Stack Overflow both include screenshots of code errors from Visual Studio. OCR extracts error messages, and image captioning describes the setup or the error context. Theoretically, these techniques should provide a richer understanding and help link duplicate questions even if their textual descriptions differ.

🔸 *Real-World Application Example*: In one test case, two questions included similar screenshots depicting a common database error. OCR successfully extracted the error codes, and the captions described the database tools being used. Despite these technological efforts, the overall system recognised these as duplicates only slightly more effectively than text-based methods alone, demonstrating a mere 1% improvement.

🔸 *Challenges and Limitations*: The complexity introduced by adding OCR and image captioning was significant, requiring extensive computational resources. For example, processing thousands of images to extract text and generate captions involved considerable processing time and power, which was not offset by the marginal gains in detection accuracy.

🔸 *Implications for AI Development*: This research highlights the importance of resource efficiency and practical value in AI innovations. It suggests a reevaluation of how and when to integrate complex AI techniques in real-world systems, especially when the cost and system overhead may outweigh the benefits.

🔸 *Future Directions and Potential*: While the results were underwhelming, the research opens avenues for exploring more sophisticated image processing techniques or perhaps a more targeted application of these methods. Future research might focus on refining the accuracy of OCR and captioning tools or integrating them with more advanced AI models to better capture the nuances of visual data.

### Reference:
Ahmed, F., Datta, S., and Nayebi, M., 2024. Negative Results of Image Processing for Identifying Duplicate Questions on Stack Overflow. arXiv:2407.05523. Available at: https://arxiv.org/abs/2407.05523 [Accessed: 31 July 2024].

