---
layout: post
title: Automatic Summarization of Doctor-Patient Dialogues Using Large Language Models
category:
- natural language processing (NLP)
- machine learning
- large language models (LLMs)
tag:
- clinical summarization
- doctor-patient dialogue
- prompt tuning
- electronic health records (EHRs)
date: 2024-09-13 18:20 -0500
pin: true
---

## Automatic Summarization of Doctor-Patient Dialogues Using Large Language Models

We explore the potential of **automatic text summarization (ATS)** in reducing the clinical documentation burden through **large language models (LLMs)**. Clinical documentation is an essential yet time-consuming task for healthcare providers. Our study focuses on summarizing **doctor-patient dialogues** into structured **clinical notes** using generative LLMs. By leveraging **prompt-tuning (P-tuning)**, we aim to develop a **computationally efficient** method that maintains high accuracy while reducing model training costs.

### Key Findings
- We demonstrate that **GatorTronGPT-20B with P-tuning outperforms traditional fine-tuning approaches**, achieving the best summarization quality across multiple evaluation metrics.
- Our results show that **prompt-tuning significantly reduces computational costs** compared to full fine-tuning, while maintaining high performance.
- **GatorTronGPT-20B-generated summaries** better capture **clinically relevant information** than T5-based fine-tuning, making it a more practical solution for real-world applications.
- We observe that **few-shot learning with as few as 200 samples** is sufficient to achieve reasonable summarization performance.

### Methodology
- **Dataset**:
  - We use the **MTS-DIALOG dataset**, a widely recognized benchmark for clinical ATS.
  - The dataset includes **1,701 doctor-patient dialogues** covering multiple medical specialties such as **general medicine, neurology, and dermatology**.
- **Models Compared**:
  - We evaluate **GatorTronGPT (5B & 20B)**, a generative LLM trained on **277 billion words** of clinical and general English text.
  - We compare against **T5-Large**, a widely used encoder-decoder model for text generation.
- **Prompt-Tuning vs Fine-Tuning**:
  - Instead of modifying the entire model, **prompt-tuning updates only soft prompts**, significantly reducing computational demands.
  - **Fine-tuning requires training the entire model**, leading to higher computational costs.

### Evaluation & Results
- **Performance Metrics**:
  - We use **ROUGE-1, ROUGE-2, ROUGE-L, BLEU, and BERTScore** to evaluate the generated summaries.
  - Our results indicate that **GatorTronGPT-20B with P-tuning outperforms T5** across all evaluation metrics.
- **Computational Efficiency**:
  - Fine-tuning **T5-Large** took **9h 34m** and required updating **770M parameters**.
  - Prompt-tuning **GatorTronGPT-20B** took only **4h 23m**, updating **302M parameters**, demonstrating its efficiency.
- **Quality of Generated Summaries**:
  - Our analysis shows that **GatorTronGPT-20B-generated summaries** retain **more clinically relevant details**, including specific conditions and medications, compared to T5.

### Implications
We demonstrate that **prompt-tuning for LLMs provides a cost-effective and high-performing solution** for clinical summarization tasks. Our approach has the potential to **reduce clinician workload, improve documentation accuracy, and enhance continuity of care**.

Moving forward, we plan to:
- Expand **P-tuning methodologies** to support **multi-task NLP applications** in healthcare.
- Improve **few-shot learning** capabilities to enhance generalization across clinical domains.
- Explore **human-in-the-loop training** to refine and validate model-generated summaries.

Publication:
- Lyu M, Peng C, Li X, Balian P, Bian J, Wu Y. *Automatic Summarization of Doctor-Patient Encounter Dialogues Using Large Language Model through Prompt Tuning.* arXiv. 2024. Available at: [https://arxiv.org/abs/2403.13089](https://arxiv.org/abs/2403.13089)
