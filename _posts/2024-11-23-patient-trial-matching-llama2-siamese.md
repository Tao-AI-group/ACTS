---
layout: post
title: Matching Patients to Clinical Trials Using LLaMA 2 Embeddings and Siamese Neural Networks
category:
- machine learning
- deep learning
- clinical trial matching
tag:
- LLaMA 2
- patient recruitment
- electronic health records (EHRs)
- Siamese neural network
date: 2024-11-23 16:31 -0500
pin: true
---

## Matching Patients to Clinical Trials Using LLaMA 2 Embeddings and Siamese Neural Networks

We explore the use of **large language models (LLMs)** and **Siamese Neural Networks (SNNs)** for **automating patient recruitment for clinical trials**. Patient recruitment is a **key challenge in clinical trial success**, with **86% of trials failing to meet recruitment goals**, leading to delays and increased costs. Our study proposes **Siamese-PTM**, a deep learning framework that utilizes **LLaMA 2 embeddings** to efficiently match patient electronic health records (EHRs) with clinical trial eligibility criteria.

### Key Findings
- **Siamese-PTM significantly improved patient-trial matching accuracy by 40% compared to rule-based methods**.
- The model leverages **LLaMA 2 embeddings** to encode both **structured and unstructured EHR data**, enhancing predictive performance.
- **Unstructured EHR data (radiology reports) proved more informative than structured clinical events**, highlighting the value of **free-text narratives** in patient eligibility prediction.
- **Fine-tuned LSTM encoders achieved the highest performance**, with an **F1-score of 0.92** on fine-grained patient-trial matching tasks.
- **Cross-validation experiments demonstrated that Siamese-PTM generalizes well** to new patient-criteria pairs.

### Methodology
- **Dataset**:
  - We used **five clinical trials** (NCT02008357, NCT04468659, NCT02669433, NCT01767909, NCT02565511) focused on **cognitive disorders (e.g., Alzheimer's Disease, Dementia with Lewy Bodies)**.
  - Patient EHR data were sourced from **Mayo Clinic's United Data Platform (UDP)**, including **structured clinical events, unstructured radiology reports, and demographic data**.
  - The dataset included **180 patients**, with **50 eligible ("success") and 130 ineligible ("fail")**.
- **Model Architecture**:
  - **Siamese-PTM employs a dual-encoder structure**, where **identical subnetworks** process **EHR and eligibility criteria separately** before merging their embeddings for final classification.
  - We experimented with **multiple encoders**, including **LSTM, GRU, CNN, and attention-based variants**.
  - **LLaMA 2 embeddings** were tested at both **token-level (fine-grained) and document-level (coarse-grained)** representations.
- **Evaluation Metrics**:
  - Performance was assessed using **F1-score, AUC-ROC, and precision-recall curves**.
  - **Comparison with rule-based classifiers** (Random Forest, SVM, Logistic Regression) was conducted.

### Evaluation & Results
- **Performance Comparison**:
  - Siamese-PTM **outperformed rule-based methods** by a **40% improvement in F1-score (p-value=0.006)**.
  - **LSTM-based encoders achieved the highest accuracy**, with **Bi-LSTM and attention-enhanced variants** further improving generalization.
  - **Structured EHR alone underperformed compared to unstructured text**, demonstrating the importance of **context-rich medical narratives**.
- **Feature Importance**:
  - **Eligibility criteria that included symptoms, medication history, and cognitive assessments were strong predictors**.
  - Siamese-PTM's ability to **learn semantic relationships between eligibility criteria and patient records** was confirmed through **t-SNE clustering analysis**.

### Implications
We demonstrate that **deep learning models, particularly Siamese Neural Networks with LLaMA 2 embeddings, can significantly enhance patient-trial matching**. This approach has the potential to:
- **Accelerate clinical trial recruitment** by reducing manual screening efforts.
- **Improve trial efficiency** by ensuring better patient-trial matches.
- **Enhance generalizability** of patient-trial matching across institutions.

### Future Work
- Expanding the model to **cross-institutional datasets** for broader applicability.
- Exploring **federated learning** to address data privacy concerns.
- Integrating **clinical reasoning models** to enhance interpretability.

Publication:
- Chowdhury S, Rajaganapathy S, Yu Y, Tao C, Vassilaki M, Zong N. *Matching Patients to Clinical Trials Using LLaMA 2 Embeddings and Siamese Neural Networks.* medRxiv. 2024. Available at: [https://doi.org/10.1101/2024.06.28.24309677](https://doi.org/10.1101/2024.06.28.24309677)
