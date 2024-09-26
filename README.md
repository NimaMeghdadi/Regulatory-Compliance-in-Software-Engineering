# Regulatory Compliance in Software Engineering using NLP

This project investigates the role of various Natural Language Processing (NLP) techniques to enhance regulatory compliance in software engineering, particularly in processing requirement documents.

## Table of Contents
- [Abstract](#abstract)
- [Dataset](#dataset)
- [Methodology](#methodology)
  - [Multi-Class Multi-Label Classification](#multi-class-multi-label-classification)
  - [Semantic Textual Similarity (STS)](#semantic-textual-similarity-sts)
  - [Prompt Engineering](#prompt-engineering)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)

## Abstract
Regulatory compliance in software engineering is essential for ensuring the integrity, security, and ethical use of software systems. This project applies three NLP approaches to analyze requirement documents:
- **Multi-Class Multi-Label Classification**
- **Semantic Textual Similarity (STS)**
- **Prompt Engineering**

## Dataset
We used the publicly available **HIPAA (Health Insurance Portability and Accountability Act)** dataset. This dataset comprises anonymized healthcare data to verify whether software solutions protect patient privacy and adhere to HIPAA regulations.

The dataset consists of:
- **Requirements**: 1891 requirements
- **Regulations**: 10 regulatory codes
- **Trace links**: 243 trace links between requirements and regulations

## Methodology
### Multi-Class Multi-Label Classification
We classified each requirement into one or more regulatory codes using the **bert-base-cased** model. This approach involved training the model with positive and negative examples, achieving the following results:

| Metric    | Score    |
|-----------|----------|
| Recall    | 42.30%   |
| Precision | 22.00%   |
| F1-Score  | 28.94%   |
| Accuracy  | 23.94%   |

### Semantic Textual Similarity (STS)
We used the **paraphrase-mpnet-base-v2** model to measure the similarity between requirements and regulations. Positive examples had a cosine similarity score of 1, while negative examples scored 0.

| Metric    | Score     |
|-----------|-----------|
| Recall    | 97.67%    |
| Precision | 100.00%   |
| F1-Score  | 98.82%    |
| Accuracy  | 98.91%    |

### Prompt Engineering
This method used the **Gemini LLM** to classify requirements based on prompt engineering with few-shot examples. We tested the model with different percentages of training data.

| Few Shots    | Recall   | Precision | F1-Score | Accuracy |
|--------------|----------|-----------|----------|----------|
| 100% Train   | 83.72%   | 85.71%    | 84.70%   | 96.88%   |
| 20% Train    | 90.69%   | 86.66%    | 88.63%   | 97.58%   |

## Results
The **STS** approach outperformed the other methods with an F1-score of 98.82% and an accuracy of 98.91%, demonstrating its effectiveness in handling regulatory compliance data.

## Conclusion
This project demonstrated the potential of NLP techniques in automating regulatory compliance checks. We found that combining prompt engineering with advanced sentence transformers like **paraphrase-mpnet-base-v2** significantly improved results, particularly in scenarios with limited training data.

## References
1. Malinowski, T., et al. (2016). Automated Compliance Checking of Legal Documents: A Natural Language Processing Approach.
2. Swamy, V., et al. (2019). Regulatory Compliance Monitoring Using Natural Language Processing.
3. Jain, S., et al. (2020). Automating Regulatory Reporting Using Natural Language Processing.
4. Rodriguez, J. A., et al. (2017). Ontology-Based Semantic Annotation of Regulatory Documents for Compliance Checking.
