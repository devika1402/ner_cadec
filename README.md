# NER in the CSIRO Adverse Drug Event Corpus

## Overview

This project focuses on **Named Entity Recognition (NER)** for **biomedical texts**, specifically on detecting **Adverse Drug Reactions (ADR)** in the **CADEC dataset**. The dataset consists of user-generated medical forum posts labeled with different medical entities.

We employ **BioBERT**, a transformer-based biomedical model, and enhance it with **Focal Loss** to address class imbalance, significantly improving the detection of rare medical entities.

---

## Key Features
- Transformer-based NER model for biomedical text classification.
- Fine-tuned BioBERT model to extract medical entities from patient-reported drug reviews.
- Focal Loss implementation to improve recognition of underrepresented entities.
- Performance evaluation based on standard metrics like Accuracy, Precision, Recall, and F1-score.

---

## Results Summary

| Metric                         | BioBERT + Cross-Entropy | BioBERT + Focal Loss |
|--------------------------------|-------------------------|----------------------|
| Accuracy                       | 88.92%                  | 89.15% (+0.23%)      |
| F1-score                       | 88.04%                  | 88.20% (+0.16%)      |
| Rare Entity (B-Finding)        | 0%                      | 21.51%               |
| Rare Entity (I-Disease)        | 1.68%                   | 17.33%               |

---

## Repository Structure
ner-ade-csiro
├── README.md              # Project documentation
├── ner_cadec.ipynb        # Jupyter Notebook with code implementation
└── models/                # Saved fine-tuned models

---

### The notebook includes:
- Data preprocessing & tokenization
- Model training (BioBERT + CrossEntropy / Focal Loss)
- Performance evaluation
- Visualization of results

---

## Model Performance

### Standard BioBERT Model (Cross-Entropy Loss)
- High overall accuracy but struggles with rare entities.

### BioBERT + Focal Loss
- Improves recognition of rare entities (e.g., diseases, symptoms, ADRs).
- Slight increase in accuracy and F1-score with better class balance.
