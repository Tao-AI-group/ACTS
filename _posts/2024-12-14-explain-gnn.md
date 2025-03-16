---
layout: post
title: Self-Explainable Graph Neural Network for Alzheimer’s Disease Risk Prediction
category:
- machine learning
- graph neural networks
- healthcare AI
tag:
- Alzheimer’s disease
- risk prediction
- graph neural networks
- explainable AI
date: 2024-12-14 10:00 -0500
pin: true
---

## Self-Explainable Graph Neural Network for Alzheimer’s Disease Risk Prediction

We introduce a **self-explainable graph neural network (GNN) framework** to enhance **Alzheimer’s disease and related dementias (ADRD) risk prediction**. With ADRD ranking among the leading causes of mortality, early and accurate risk assessment is critical for **timely interventions, improved patient outcomes, and optimized healthcare strategies**. Our approach, leveraging **graph-based deep learning**, not only **outperforms conventional machine learning models** but also offers **interpretability**, making it an invaluable tool for clinicians and researchers.

### Key Findings
- **Graph-based models significantly outperformed traditional machine learning models (Random Forest and LightGBM)**, achieving up to **10.6% improvement in AUROC scores**.
- **The proposed variationally regularized encoder-decoder GNN (VGNN) framework successfully captures relationships among diverse medical codes**, improving ADRD prediction accuracy.
- **Our self-explainable relation importance method identifies key medical code interactions** that either contribute to or mitigate ADRD risk.
- **Routine healthcare interactions (such as preventive care and cataract procedures) were associated with lower ADRD risk**, while **substance-related disorders and electrocardiograms were linked to higher risk**.
- **Graph-based deep learning unlocks new insights into ADRD progression by uncovering meaningful patterns in claims data**.

### Methodology
- **Dataset**:
  - We used **Optum Clinformatics Data Mart (2007-2020)**, covering **over 68 million patient records**.
  - Patients were classified based on **Alzheimer’s-related diagnosis codes and prescribed medications**.
  - The study cohort included **432,374 ADRD patients and 1,895,511 controls**, filtered for individuals aged **65 and older**.
- **Model Architecture**:
  - We developed a **variationally regularized GNN (VGNN)** to predict ADRD likelihood using **claims data**.
  - **Graph attention layers capture interconnections between diagnosis codes, procedures, and medications**, creating a structured medical graph per patient.
  - **Relation importance interpretation** allows real-time feature explanation without requiring post-hoc methods.
- **Evaluation Metrics**:
  - **Performance was measured using AUROC, precision-recall curves, and comparison with tree-based classifiers**.
  - **Models were tested across three prediction windows (1-year, 2-year, and 3-year risk assessment scenarios)**.

### Evaluation & Results
- **VGNN outperformed baseline models (Random Forest and LightGBM) across all scenarios**, with **an AUROC improvement of up to 10.6%**.
- **Top Features Impacting ADRD Prediction**:
  - **Protective Factors**: Routine checkups, cataract surgery, and hypertension treatments (e.g., calcium channel blockers) correlated with lower ADRD risk.
  - **Risk Factors**: Substance-related disorders, diagnostic imaging procedures, and cardiovascular assessments (e.g., electrocardiograms) were linked to higher ADRD risk.
- **Model Interpretability**:
  - The **relation importance method highlighted medical code pairs** contributing to ADRD outcomes.
  - **Graph-based insights aligned with prior clinical research**, validating our approach.

### Implications
We demonstrate that **graph neural networks offer a powerful, interpretable approach to ADRD risk prediction**, enabling:
- **More precise patient stratification for early intervention and clinical trials**.
- **Reduced manual screening efforts for ADRD risk assessments**.
- **Scalability to broader healthcare datasets for population-level disease modeling**.

### Future Work
- **Expanding the model to real-world clinical settings**, incorporating EHR and imaging data.
- **Integrating temporal modeling techniques** for enhanced predictive accuracy.
- **Exploring federated learning approaches** to ensure data privacy while improving model generalization.

Publication:
- Hu X, Sun Z, Nian Y, Wang Y, Dang Y, Li F, Feng J, Yu E, Tao C. *Self-Explainable Graph Neural Network for Alzheimer’s Disease Risk Prediction.* JMIR Aging. 2024. Available at: [https://doi.org/10.2196/54748](https://doi.org/10.2196/54748)
