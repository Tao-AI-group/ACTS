---
layout: post
title: Identifying Cancer Patients at Risk of Heart Failure Using Large Language Models
category:
- real world data (RWD)
- machine learning
- large language models (LLMs)
tag:
- cancer
- heart failure
- electronic health records
- deep learning
date: 2024-08-22 08:33 -0500
pin: true
---

## Identifying Cancer Patients at Risk of Heart Failure Using Large Language Models

Cancer treatments often introduce cardiotoxicity, increasing the risk of heart failure (HF) among cancer patients. This study explored the potential of machine learning (ML) models and large language models (LLMs) to identify cancer patients at risk of HF using electronic health records (EHRs). A cohort of **12,806** cancer patients diagnosed with lung, breast, and colorectal cancers was extracted from the University of Florida Health database, among which **1,602** patients developed HF after their cancer diagnosis.

### Key Findings
- **GatorTron-3.9B**, an LLM trained on biomedical and clinical texts, outperformed traditional ML models such as **Support Vector Machines (SVMs)** and **XGBoost (XGB)**, as well as deep learning-based **Time-Aware LSTM (T-LSTM)**.
- The **F1-score** of GatorTron-3.9B was **39% higher than SVMs**, **7% higher than T-LSTM**, and **5.6% higher than BERT**.
- A novel **subword feature representation** significantly improved model performance compared to traditional one-hot encoding and sequence-based representations in LSTMs.
- The model showed strong performance across different cancer subtypes, with the highest accuracy in **patients with multiple cancer types**.

### Methodology
- Patients' structured EHR data were transformed into three feature representations:
  - **One-hot encoding** for traditional ML models.
  - **Sequence-based encoding** for T-LSTM.
  - **Subword representation** for LLMs (using official descriptions of structured codes).
- Models were trained and validated on separate datasets, using **F1-score** as the primary evaluation metric.
- Feature importance analysis using **LIME (Local Interpretable Model-Agnostic Explanations)** highlighted key predictive factors such as **abnormal electrocardiograms (ECGs)** and specific medications.

### Implications
This study demonstrates the **effectiveness of LLMs in risk prediction for complex medical conditions**, suggesting that subword features derived from structured EHRs can serve as a **bridge between structured and unstructured medical data**. The approach can enhance **early detection of HF risk** in cancer patients, improving treatment decisions and patient outcomes.

Publication:
- Chen Z, Zhang M, Ahmed MM, Guo Y, George TJ, Bian J, Wu Y. *Narrative Feature or Structured Feature? A Study of Large Language Models to Identify Cancer Patients at Risk of Heart Failure.* arXiv. 2024. Available at: [https://arxiv.org/abs/2403.11425](https://arxiv.org/abs/2403.11425)
