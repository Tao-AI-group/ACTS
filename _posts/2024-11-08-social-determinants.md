---
layout: post
title: Large Language Models for Social Determinants of Health Extraction
category:
- natural language processing (NLP)
- machine learning
- large language models (LLMs)
tag:
- social determinants of health (SDoH)
- electronic health records (EHRs)
- multi-label classification
- transfer learning
date: 2024-11-08 20:33 -0500
pin: true
---

## Large Language Models for Social Determinants of Health Extraction

We investigate the use of **large language models (LLMs)** for extracting **social determinants of health (SDoH)** from **electronic health records (EHRs)**. SDoH factors such as **income, housing stability, education, and social support** play a critical role in health outcomes, yet much of this information is buried within unstructured clinical notes. Our study focuses on developing **generalizable models** capable of extracting a wide range of SDoH factors across multiple healthcare institutions.

### Key Findings
- We developed a **cross-institutional dataset** containing clinical notes from **four healthcare systems**:  
  - **Harris County Psychiatric Center (HCPC)**  
  - **University of Texas Physician Practice (UTP)**  
  - **Beth Israel Deaconess Medical Center (MIMIC-III)**  
  - **Mayo Clinic**
- Our study introduced a **multi-label classification approach** to extract **21 SDoH factors**, ranging from **housing and employment status** to **adverse childhood experiences and financial difficulties**.
- We compared **four models**:  
  - **XGBoost (traditional ML)**  
  - **TextCNN (deep learning)**  
  - **Sentence-BERT (SBERT, transformer-based model)**  
  - **LLaMA (instruction-tuned LLM)**
- **LLaMA achieved the highest performance**, with **F1 scores exceeding 0.9 on single-institution datasets** and **above 0.84 on cross-institution datasets**.
- While models performed well within single datasets, **cross-dataset generalization remains a challenge**, with notable drops in performance.

### Methodology
- **Datasets & Annotation**:
  - We curated **four distinct corpora of clinical notes**, covering **inpatient and outpatient settings**.
  - Clinical notes were manually annotated at **two levels**:  
    - **Level 1**: SDoH factor presence (e.g., "housing instability").  
    - **Level 2**: Factor values (e.g., "homeless", "renting").
- **Model Training & Evaluation**:
  - We framed the problem as a **multi-label classification task**, allowing models to detect **multiple SDoH factors** per sentence.
  - We assessed model performance using **micro-averaged precision, recall, and F1 scores**.
  - Cross-dataset experiments evaluated model **generalizability** across institutions.

### Evaluation & Results
- **Performance Comparison**:
  - **LLaMA consistently outperformed other models**, particularly in cross-institutional tasks.
  - **SBERT and XGBoost showed competitive results within single datasets** but struggled with generalization.
  - **TextCNN exhibited lower performance**, especially on datasets with high variability in documentation practices.
- **Computational Considerations**:
  - **LLaMA models require significant computational resources**, but **instruction tuning enhances efficiency**.
  - **Traditional ML models (XGBoost) remain viable for resource-limited settings**.

### Implications
We demonstrate that **LLMs can effectively extract complex SDoH factors from unstructured clinical text**, offering **a scalable solution** for improving patient risk assessment and health equity research. However, **cross-institutional generalizability challenges persist**, highlighting the need for:
- **Better domain adaptation strategies** for LLMs.
- **Federated learning approaches** to train models on decentralized datasets.
- **Improved annotation frameworks** to capture nuanced SDoH factors.

### Future Work
- Expanding datasets to include **additional healthcare institutions and note types**.
- Exploring **semi-supervised and few-shot learning** to improve cross-domain generalization.
- Developing **interpretable AI techniques** for explaining model predictions.

Publication:
- Keloth VK, Selek S, Chen Q, Gilman C, Fu S, Dang Y, Chen X, Hu X, Zhou Y, He H, Fan JW, Wang K, Brandt C, Tao C, Liu H, Xu H. *Large Language Models for Social Determinants of Health Information Extraction from Clinical Notes – A Generalizable Approach across Institutions.* medRxiv. 2024. Available at: [https://doi.org/10.1101/2024.05.21.24307726](https://doi.org/10.1101/2024.05.21.24307726)
