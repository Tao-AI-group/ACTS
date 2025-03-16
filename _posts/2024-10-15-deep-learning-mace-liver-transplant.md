---
layout: post
title: Deep Learning-Based Prediction of Cardiovascular Events After Liver Transplantation
category:
- healthcare AI
- machine learning
- deep learning
tag:
- cardiovascular events
- liver transplantation
- predictive modeling
- real-world data
date: 2024-10-15 12:11 -0500
pin: true
---

## Deep Learning-Based Prediction of Cardiovascular Events After Liver Transplantation

We investigate the use of **deep learning models** for predicting **major adverse cardiovascular events (MACE)** following **liver transplantation (LT)**. Cardiovascular disease has become a leading cause of early mortality post-LT, necessitating accurate risk prediction methods. Our study leverages **longitudinal claims data** and deep learning techniques to identify high-risk patients and improve post-transplant care.

### Key Findings
- We developed a **deep learning model (BiGRU)** that achieved an **AUC-ROC of 0.841** and an **AUC-PR of 0.578** for predicting MACE within 30 days post-LT.
- Our model **outperformed traditional machine learning models**, including **logistic regression, random forest, and light gradient boosting machine (LGBM)**.
- We found that **pre-transplant risk factors**, such as age, hypertension, diabetes, and prior myocardial infarction, were strong predictors of post-transplant MACE.
- The model demonstrated **high predictive performance across multiple time intervals** (30 days, 1 year, 3 years, and 5 years post-transplant).

### Methodology
- **Dataset**:
  - We utilized **Optum’s de-identified Clinformatics Data Mart Database**, covering **22,522** liver transplant recipients from **2007 to 2020**.
  - The final study cohort consisted of **18,304** patients after applying eligibility criteria.
- **Prediction Task**:
  - We predicted the occurrence of **MACE (heart failure, atrial fibrillation, stroke, pulmonary embolism, myocardial infarction, and cardiac arrest)** at four post-transplant intervals: **30 days, 1 year, 3 years, and 5 years**.
- **Model Architecture**:
  - We employed a **Bidirectional Gated Recurrent Unit (BiGRU)** model to **capture temporal dependencies** in patient data.
  - The BiGRU model aggregated patient medical history over a **3-year observation period before transplantation**.
  - Comparative models included **logistic regression, random forest, and LGBM**.
- **Evaluation Metrics**:
  - **AUC-ROC (Receiver Operating Characteristic)** and **AUC-PR (Precision-Recall Curve)** were used to assess model performance.

### Evaluation & Results
- **Performance Comparison**:
  - The **BiGRU model outperformed all baseline machine learning models**, particularly in short-term prediction (30 days post-transplant).
  - The **highest AUC-ROC was 0.841** for 30-day prediction, while **AUC-PR reached 0.578**.
- **Feature Importance Analysis**:
  - We identified **key predictors** of post-transplant MACE, including **hypertension, diabetes, dyslipidemia, prior myocardial infarction, and pulmonary hypertension**.
  - Medications such as **furosemide, warfarin, and spironolactone** were associated with elevated risk.

### Implications
We demonstrate that **deep learning models trained on longitudinal claims data can effectively predict post-transplant cardiovascular risks**. This approach can assist clinicians in **identifying high-risk patients** and developing targeted **risk stratification and preventive strategies**.

Future work will focus on:
- Expanding the model to incorporate **multi-modal patient data** (e.g., lab results, imaging).
- Enhancing interpretability with **explainable AI techniques**.
- **Validating the model across multiple healthcare institutions** for broader applicability.

Publication:
- Abdelhameed A, Bhangu H, Feng J, Li F, Hu X, Patel P, Yang L, Tao C. *Deep Learning-Based Prediction Modeling of Major Adverse Cardiovascular Events After Liver Transplantation.* Mayo Clin Proc Digit Health. 2024. Available at: [https://doi.org/10.1016/j.mcpdig.2024.03.005](https://doi.org/10.1016/j.mcpdig.2024.03.005)
