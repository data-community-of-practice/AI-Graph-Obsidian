
Interesting findings from "Improving Robustness of Diffusion-Based Zero-Shot Speech Synthesis via Stable Formant Generation"

Article Link : https://arxiv.org/abs/2409.09311

Zero-shot speech synthesis, which allows generating speech from unseen speakers using just a single sample, has become increasingly important in custom voice applications. However, current diffusion-based models often struggle with pronunciation stability, particularly when handling complex speech inputs. This paper identifies the critical issue of unstable pronunciation and addresses it by incorporating formant stability using source-filter theory in the diffusion process.

Novelty: The researchers propose StableForm-TTS, a novel zero-shot TTS (Text-to-Speech) framework that leverages source-filter theory to generate stable formants—key elements in producing accurate and natural speech. This model focuses on two core improvements:
1) Pronunciation accuracy: By embedding the source-filter theory, the model ensures the formants (essential components of sound production) remain stable throughout the diffusion process.
2) Scalability: StableForm-TTS not only enhances accuracy but also scales effectively, delivering comparable results to state-of-the-art models with fewer parameters.

Key Findings:
1) Pronunciation Accuracy: StableForm-TTS improves pronunciation robustness, significantly reducing the character error rate (CER) and word error rate (WER) compared to existing models.
2) Naturalness: The model also enhances the naturalness of speech synthesis, achieving better MOS (Mean Opinion Score) ratings for speech quality across various test datasets.
3) Scalability: StableForm-TTS scales effectively with larger datasets, maintaining performance while using fewer parameters than competing models.

This paper marks a significant advancement in zero-shot TTS by addressing the persistent issue of pronunciation instability. With its novel use of source-filter theory and stable formant generation, StableForm-TTS sets a new standard for generating accurate and natural speech in zero-shot scenarios.

Reference : Han, C., Lee, S., Nam, G., & Chae, G. (2024). Improving Robustness of Diffusion-Based Zero-Shot Speech Synthesis via Stable Formant Generation. _ArXiv_. /abs/2409.09311