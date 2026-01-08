# Abstractive Text Summarization using PEGASUS

This project implements an **abstractive text summarization system** using state-of-the-art **Natural Language Processing (NLP)** techniques. The system leverages the **PEGASUS transformer model** to generate concise, human-like summaries from conversational text data.

This was a **team-based academic project** developed as part of the *Human-Centred Natural Language Processing* course, combining research, model development, and full-stack deployment.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Team Members](#team-members)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Model & Methodology](#model--methodology)
- [Preprocessing & Tokenization](#preprocessing--tokenization)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [System Architecture](#system-architecture)
- [UI Integration](#ui-integration)
- [Limitations](#limitations)
- [Future Work](#future-work)
- [References](#references)

---

## Project Overview

Text summarization is a critical NLP task aimed at reducing large volumes of text into shorter versions while preserving essential information.  
This project focuses on **abstractive summarization**, where summaries are *generated* rather than directly extracted from the source text.

The PEGASUS model is used due to its strong performance on summarization benchmarks and its specialized pretraining strategy for summarization tasks.

---

## Team Members

This project was collaboratively developed by the following team members:

- Chinu Mangal  
- Debapriya Roy  
- Harshit Kumar Tyagi  
- Piyush Vikas  
- Shweta Bambal  
- Vishal Rajesh Kushwaha  

**Supervisors:**
- Dr. Marco Polignano  
- Dr. Purificato  
- Prof. Deluca  

Each team member contributed across research, model development, evaluation, and system integration.

---

## Objectives

- Develop an **abstractive text summarization system** using the PEGASUS model  
- Utilize the SAMSum dataset for training and evaluation  
- Generate fluent, coherent, and context-aware summaries  
- Evaluate performance using **ROUGE metrics**  
- Deploy the model with an interactive web-based interface  

---

## Dataset

- **Dataset:** SAMSum (Hugging Face Datasets)
- **Domain:** Conversational dialogue
- **Structure:**
  - `dialogue`: Input conversational text
  - `summary`: Human-written abstractive summary
- **Splits:** Train, Validation, Test

---

## Model & Methodology

- **Model:** PEGASUS (Transformer-based Encoder–Decoder)
- **Frameworks:**
  - Hugging Face `transformers`
  - Hugging Face `datasets`

PEGASUS uses sentence-level masking during pretraining, allowing it to better capture document-level semantics and generate high-quality abstractive summaries.

---

## Preprocessing & Tokenization

- Dataset loading using the `datasets` library
- Tokenization with `AutoTokenizer` (PEGASUS-compatible)
- Conversion to `input_ids`, `attention_masks`, and `labels`
- Batch preparation for efficient training and inference

---

## Evaluation Metrics

The model was evaluated using **ROUGE** metrics:

| Metric   | Recall | Precision | F1 Score |
|--------|--------|-----------|----------|
| ROUGE-1 | 26.8%  | 19.3%     | 19.3%    |
| ROUGE-2 | 18.2%  | 10.4%     | 12.7%    |
| ROUGE-L | 24.8%  | 17.3%     | 22.3%    |

---

## Results

- Effective abstraction with strong semantic retention  
- Robust performance across varying dialogue lengths  
- Significant reduction in text length while preserving meaning  
- Coherent and human-like generated summaries  

---

## System Architecture

- **Backend:** Flask (Python)
- **Frontend:** React.js

**Workflow:**
1. User inputs text
2. Flask API processes request
3. PEGASUS generates summary
4. Summary returned to frontend UI

---

## UI Integration

- Simple and intuitive interface
- Supports real-time text summarization
- Designed for demonstration and usability

---

## Limitations

- Limited domain coverage of the SAMSum dataset  
- Fine-tuning large transformer models is computationally expensive  
- Performance may degrade on very long or highly technical documents  

---

## Future Work

- Multimodal summarization  
- Domain-specific summarization  
- Cross-lingual summarization  
- Ethical bias detection and mitigation  
- Chatbot and conversational AI integration  

---

## References

Key references include PEGASUS, SAMSum, and foundational NLP summarization literature as cited in the project documentation.




This repository is intended for **academic and educational use**.  
Please provide appropriate credit if used in research or derivative projects.
