---
layout: post
title: Improving Generalizability of Social Determinants of Health Extraction Using Large Language Models
category:
- natural language processing (NLP)
- machine learning
- large language models (LLMs)
tag:
- social determinants of health (SDoH)
- prompt tuning
- transfer learning
- electronic health records
date: 2024-09-09 17:56 -0500
pin: true
---

## Improving Generalizability of Social Determinants of Health Extraction Using Large Language Models

The ability to extract Social Determinants of Health (SDoH) from clinical narratives is crucial for understanding patient backgrounds and improving healthcare delivery. Traditional fine-tuning of transformer-based models has demonstrated **limited transferability** across institutions and diseases. This study explores **prompt-tuning (P-tuning)** as an alternative to enhance generalizability, comparing **encoder-only (GatorTron) and decoder-only (GatorTronGPT) architectures**.

### Key Findings
- **P-tuning significantly improves transfer learning** for extracting SDoH concepts and relations across different institutions and diseases.
- **GatorTronGPT-20B with P-tuning** achieved the best **F1 scores**, outperforming fine-tuned BERT and GatorTron by:
  - **21.8% in cross-institution settings**
  - **14.5% in cross-disease settings**
- **Generative LLMs (GatorTronGPT) perform better** than encoder-only LLMs (GatorTron) for cross-domain SDoH extraction.
- Larger LLMs with billions of parameters benefited **more from P-tuning**, while smaller models (e.g., GatorTron-345M) showed performance gaps.

### Methodology
- **Datasets**:
  - **Cross-institution evaluation**: 2022 n2c2 challenge dataset (MIMIC-III & UW clinical notes).
  - **Cross-disease evaluation**: UF Health notes (cancer vs. opioid use cohorts).
- **Models Compared**:
  - Fine-tuned **BERT** and **GatorTron** (traditional supervised learning).
  - **P-tuned GatorTron & GatorTronGPT**, updating only soft prompts while keeping model weights frozen.
- **Evaluation Metrics**:
  - **Micro-averaged strict F1-score** was the primary metric.
  - End-to-end extraction of both **concepts** and **relations**.

### Implications
This study highlights **P-tuning as a superior alternative** to traditional fine-tuning for **cross-institution and cross-disease generalization** in clinical NLP. The findings suggest that **generative models (GatorTronGPT) are more robust** than encoder-only models (GatorTron) in handling transfer learning scenarios.

Future work will focus on:
- Expanding P-tuning strategies to other **clinical NLP tasks**.
- Exploring **larger generative models** beyond GatorTronGPT.
- Developing **more efficient P-tuning** techniques to reduce computational costs.

Publication:
- Peng C, Yu Z, Smith KE, Lo-Ciganic W, Bian J, Wu Y. *Improving Generalizability of Extracting Social Determinants of Health Using Large Language Models through Prompt-tuning.* arXiv. 2024. Available at: [https://arxiv.org/abs/2403.12374](https://arxiv.org/abs/2403.12374)
