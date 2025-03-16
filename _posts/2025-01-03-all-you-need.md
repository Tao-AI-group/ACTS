---
layout: post
title: Generative Large Language Models Are All-purpose Text Analytics Engines: Text-to-text Learning Is All You Need
category:
- machine learning
- natural language processing
- clinical NLP
tag:
- generative LLMs
- text-to-text learning
- prompt tuning
- clinical concept extraction
date: 2025-01-03 14:57 -0500
pin: true
---

## Generative Large Language Models Are All-purpose Text Analytics Engines: Text-to-text Learning Is All You Need

We explore how **generative large language models (LLMs)** can serve as **universal text analytics engines** for clinical natural language processing (NLP). By **formulating diverse NLP tasks as text-to-text problems**, our approach eliminates the need for task-specific models, **achieving state-of-the-art performance on five out of seven major clinical NLP tasks** using a **single, unified generative model**.

### Key Findings
- **GatorTronGPT (20B parameters) outperformed task-specific transformer models** by up to **10% on clinical NLP tasks**.
- **Soft prompt tuning with frozen LLMs proved highly effective**, improving **generalization across datasets** while reducing computational costs.
- **Concept extraction and relation extraction performance improved by 3-7%**, significantly enhancing **social determinants of health (SDoH) data processing**.
- **Soft prompting outperformed traditional fine-tuning approaches**, demonstrating that **one generative LLM can replace multiple task-specific models**.
- **Clinical abbreviation disambiguation saw an F1-score increase of 3.4-10%**, confirming **LLM versatility in text standardization**.

### Methodology
- **Dataset**:
  - We evaluated **seven major clinical NLP tasks**, including **concept extraction, relation extraction, clinical abbreviation disambiguation, and progress note understanding**.
  - Data sources included **MIMIC-III, MedNLI, n2c2 challenges, and SemEval-2015**.
- **Model Architecture**:
  - We utilized **GatorTronGPT, a generative LLM trained on 277 billion words of clinical and general text**, with **5B and 20B parameter variants**.
  - **Soft prompt tuning** enabled the **frozen LLM to adapt to different tasks** without modifying model weights.
- **Evaluation Metrics**:
  - **F1-score, accuracy, precision-recall curves, and AUROC**.
  - Performance was **benchmarked against transformer-based models**, including **BERT, RoBERTa, and GatorTron-MRC**.

### Evaluation & Results
- **Unified generative LLMs outperformed task-specific models** across most NLP tasks.
- **Concept and relation extraction** saw **3-7% improvements over previous benchmarks**.
- **Natural language inference accuracy increased by 5.5-9%**, validating LLMs' reasoning capabilities.
- **Training costs were reduced by up to 94%** using **soft prompts instead of fine-tuning**.
- **Minimal performance degradation when scaling across institutions**, proving **LLM robustness for cross-hospital deployment**.

### Implications
We demonstrate that **one generative LLM, tuned with soft prompts, can replace multiple task-specific models**, enabling:
- **Scalable, cost-effective clinical NLP solutions** with **minimal retraining overhead**.
- **Improved generalization** for tasks requiring clinical text understanding.
- **Easier deployment of AI-powered healthcare applications** without model-specific adjustments.

### Future Work
- **Scaling the model for multi-task instruction learning** to further improve generalization.
- **Exploring federated learning approaches** to address **privacy concerns in clinical data**.
- **Integrating domain adaptation techniques** for **real-world healthcare applications**.

Publication:
- Peng C, Yang X, Chen A, Yu Z, Smith KE, Costa AB, Flores MG, Bian J, Wu Y. *Generative Large Language Models Are All-purpose Text Analytics Engines: Text-to-text Learning Is All You Need.* arXiv. 2024. Available at: [https://arxiv.org/abs/2312.06099](https://arxiv.org/abs/2312.06099)
