---
layout: post
title: Model Tuning or Prompt Tuning? A Study of Large Language Models for Clinical Concept and Relation Extraction
category:
- machine learning
- natural language processing
- healthcare AI
tag:
- large language models
- clinical NLP
- prompt tuning
- relation extraction
date: 2024-12-28 12:18 -0500
pin: true
---

## Model Tuning or Prompt Tuning? A Study of Large Language Models for Clinical Concept and Relation Extraction

We investigate the effectiveness of **soft prompt tuning** versus **model tuning** for clinical concept and relation extraction using **large language models (LLMs)**. With the increasing adoption of **transformer-based NLP models** in healthcare, optimizing training strategies is crucial for **scalability, efficiency, and generalizability**. Our study systematically evaluates **four tuning strategies**, demonstrating that **soft prompting with frozen LLMs significantly reduces computational costs while maintaining high performance**.

### Key Findings
- **Soft prompting with frozen GatorTron-8.9B achieves state-of-the-art performance in cross-institution generalization**, outperforming traditional fine-tuning.
- **Unfrozen LLMs perform slightly better within the same dataset**, but frozen LLMs generalize significantly better across institutions.
- **Frozen LLMs reduce training costs by up to 94%**, making them highly scalable for real-world clinical applications.
- **GatorTron-3.9B and GatorTron-8.9B outperform smaller models**, confirming that **larger LLMs compensate for the limitations of frozen training**.
- **Soft prompts outperform manually designed hard prompts**, demonstrating the advantage of machine-learned embeddings.

### Methodology
- **Dataset**:
  - Two benchmark clinical datasets:
    - **2018 n2c2 Drug-ADE dataset** (medication and adverse drug event extraction).
    - **2022 n2c2 Social Determinants of Health (SDoH) dataset** (health disparities and social factors).
  - **Cross-institution evaluation:** Models were trained on **MIMIC-III data** and tested on **University of Washington (UW) clinical notes**.
- **Model Variants**:
  - **GatorTron-345M, GatorTron-3.9B, and GatorTron-8.9B** compared with **BERT, RoBERTa, and clinical-specific models**.
- **Tuning Strategies**:
  - **Fine-tuning without prompts (baseline)**.
  - **Hard prompting with unfrozen LLMs** (manual text prompts).
  - **Soft prompting with unfrozen LLMs** (trainable embeddings).
  - **Soft prompting with frozen LLMs** (parameters remain unchanged, only prompt embeddings are trained).
- **Evaluation Metrics**:
  - **F1-score, AUC-ROC, precision-recall curves**.
  - **Few-shot learning ability** (performance with minimal training data).

### Evaluation & Results
- **Concept Extraction**:
  - **Soft prompting with frozen GatorTron-8.9B** outperformed fine-tuned models in **cross-institution settings**, achieving an **F1-score of 0.8588**.
  - **Within the same dataset, unfrozen models performed slightly better**, but required significantly more computational resources.
- **Relation Extraction**:
  - **Frozen LLMs improved generalization to new clinical environments**, outperforming traditional fine-tuning by **1.6% on UW-test**.
  - **Soft prompting enhanced few-shot learning**; **GatorTron-8.9B achieved 81.6% accuracy using just 100 training samples**.
- **Computational Efficiency**:
  - **Frozen LLMs reduced training costs to 2.5%–6% of fine-tuning approaches**, enabling **scalability in real-world applications**.

### Implications
We demonstrate that **soft prompt tuning with frozen large language models is a scalable and efficient alternative to traditional model tuning**. These findings suggest:
- **Deploying a single frozen LLM with soft prompts for multiple clinical tasks**, reducing maintenance costs.
- **Enhancing cross-institution model generalization**, enabling AI-driven healthcare solutions across diverse datasets.
- **Optimizing computational efficiency**, making LLM adoption feasible in hospital settings.

### Future Work
- **Extending soft prompt tuning to generative LLMs** (e.g., GPT-4, T5) for broader clinical NLP tasks.
- **Exploring hybrid prompt tuning techniques** to balance model performance and computational cost.
- **Investigating domain adaptation strategies** for fine-tuning LLMs on specialized clinical subfields.

Publication:
- Peng C, Yang X, Smith KE, Yu Z, Chen A, Bian J, Wu Y. *Model Tuning or Prompt Tuning? A Study of Large Language Models for Clinical Concept and Relation Extraction.* Journal of Biomedical Informatics. 2024. Available at: [https://doi.org/10.1016/j.jbi.2024.104630](https://doi.org/10.1016/j.jbi.2024.104630)
