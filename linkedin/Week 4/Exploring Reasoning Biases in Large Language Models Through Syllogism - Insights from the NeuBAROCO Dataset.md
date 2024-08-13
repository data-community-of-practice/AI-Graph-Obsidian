# Exploring Reasoning Biases in Large Language Models Through Syllogism - Insights from the NeuBAROCO Dataset

Large Language Models (LLMs) such as GPT-3 and BERT have revolutionized natural language processing, demonstrating impressive capabilities across a range of tasks. However, their performance in logical reasoning, particularly syllogistic reasoning, remains suboptimal. Syllogistic reasoning requires the model to draw a logical conclusion from two or more premises, a task that often exposes reasoning biases within LLMs. This paper investigates these biases through the lens of the NeuBAROCO dataset, a novel and comprehensive dataset designed to evaluate LLMs' performance on syllogistic reasoning tasks.

**Article Link** : https://arxiv.org/abs/2408.04403

## Understanding the Problem

Syllogistic reasoning is a fundamental component of human logic, involving the deduction of conclusions from two premises that share a common term. For example, given the premises:

- **Premise 1:** All mammals are animals.
- **Premise 2:** All dogs are mammals.

A logically sound conclusion would be:

- **Conclusion:** Therefore, all dogs are animals.

While this may seem straightforward, LLMs often struggle with similar tasks. The paper highlights that LLMs tend to misinterpret the structure of syllogisms, leading to incorrect conclusions. For instance, when presented with:

- **Premise 1:** Some mammals are animals.
- **Premise 2:** All dogs are mammals.

An incorrect model output might conclude:

- **Incorrect Conclusion:** Therefore, all dogs are animals.

This example illustrates a common reasoning bias where the model fails to differentiate between universal and particular premises, leading to erroneous generalizations.

## Methodology

The paper introduces the **NeuBAROCO dataset**, specifically designed to evaluate and analyze the syllogistic reasoning capabilities of LLMs. By systematically testing the models across various syllogistic tasks, the study identifies patterns of reasoning errors and biases. The introduction of this dataset is a critical contribution, offering a standardized way to assess and improve the logical reasoning performance of LLMs.

For instance, the dataset includes:

- **Premise 1:** All cats are animals.
- **Premise 2:** No animals are machines.
- **Conclusion:** No cats are machines.

This setup helps in identifying biases like the *atmosphere effect bias*, where the presence of a negative premise may lead to an incorrect negative conclusion. The NeuBAROCO dataset captures such nuanced errors, providing a robust framework for identifying and quantifying reasoning biases.

## Key Findings

The paper's analysis reveals several critical insights:

- **Error Patterns:** LLMs are prone to specific error patterns, such as the affirmation of the consequent and denial of the antecedent. For example, given premises that logically should not support a conclusion, LLMs sometimes incorrectly affirm the conclusion due to training biases that favor certain linguistic patterns.

- **Confirmation Bias:** LLMs often exhibit confirmation bias, where they favor conclusions that align with the more frequently observed premises in the training data. For instance, in scenarios where the premises suggest a less likely conclusion, the model might default to a more 'common' conclusion based on its training data rather than following logical deduction.

- **Sensitivity to Linguistic Cues:** The study also found that LLMs are highly sensitive to the linguistic phrasing of premises. Minor changes in wording, such as substituting "all" with "some," can significantly alter the model's conclusion, highlighting a reliance on surface-level linguistic cues rather than deep logical reasoning.

## Conclusion and Future Challenges

The paper concludes by emphasizing the need for more sophisticated training methodologies that can mitigate the identified reasoning biases. While the NeuBAROCO dataset provides a valuable tool for evaluation, it also underscores the limitations of current LLMs in logical reasoning tasks. Future research should focus on developing models that integrate formal logic frameworks, ensuring that LLMs can handle syllogistic reasoning with greater consistency and accuracy.

## Paper Reference

Ozeki, K., Ando, R., Morishita, T., Abe, H., Mineshima, K., & Okada, M., 2024, "Exploring Reasoning Biases in Large Language Models Through Syllogism - Insights from the NeuBAROCO Dataset". ArXiv. /abs/2408.04403
