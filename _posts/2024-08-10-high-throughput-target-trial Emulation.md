---
layout: post
title: High-throughput Target Trial Emulation for Alzheimer’s Disease Drug Repurposing
category:
- real world data (RWD)
- target trial emulation
tag:
- drug repurposing
- Alzheimer’s disease
- machine learning
- real-world evidence
date: 2024-08-10 13:06 -0500
pin: true
---

## High-throughput Target Trial Emulation for Alzheimer’s Disease Drug Repurposing

In this study, we employed a high-throughput target trial emulation pipeline to explore the repurposing potential of approved drugs for Alzheimer’s Disease (AD). Using two large-scale real-world data (RWD) repositories—OneFlorida and MarketScan—we analyzed over 4,300 unique drugs and conducted 430,000 emulated trials spanning more than 170 million patients’ clinical records over a 10-year period.

Our methodology leveraged machine learning-based propensity score (ML-PS) models under the inverse probability of treatment weighting (IPTW) framework to balance covariates in observational data and estimate treatment effects. We compared various ML-PS models, including logistic regression, gradient-boosted machines, multi-layer perceptrons, and long short-term memory networks with attention mechanisms. Notably, we found that simpler regularized logistic regression-based PS models outperformed more complex deep learning models in balancing baseline covariates.

Key findings from our trial emulations identified five promising drug candidates for AD repurposing: **pantoprazole, gabapentin, atorvastatin, fluticasone, and omeprazole**. These drugs demonstrated a statistically significant association with reduced AD risk among mild cognitive impairment (MCI) patients in a five-year follow-up period across both RWD datasets. Our approach offers a scalable and systematic way to generate and validate drug repurposing hypotheses, potentially accelerating real-world evidence generation in pharmaceutical research.

We plan to refine our approach by incorporating additional RWD sources, enhancing causal inference techniques, and exploring time-varying exposures. Our methodology can be broadly applied to other diseases beyond AD.

Publication:
- Zang C, Zhang H, Xu J, Zhang H, Fouladvand S, Havaldar S, Cheng F, Chen K, Chen Y, Glicksberg BS, Chen J, Bian J, Wang F. *High-throughput target trial emulation for Alzheimer’s disease drug repurposing with real-world data.* Nat Commun. 2023;14:8180. doi: [10.1038/s41467-023-43929-1](https://doi.org/10.1038/s41467-023-43929-1).

