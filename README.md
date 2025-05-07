# Symptomatic-disease-analysis
Textual Symptom Understanding using ZSL and FSL for Clinical Predictions
![WhatsApp Image 2025-04-28 at 15 10 11_8e8088ed](https://github.com/user-attachments/assets/8799579f-e6c0-40db-bac2-248461460bbf)

# Disease Prediction from Symptom Descriptions using NLP Models

This repository contains the code and implementation for disease prediction from patient-generated symptomatic descriptions using five distinct NLP models: **BART**, **BioBERT**, **CNN**, **FLAN-T5**, and **BioClinicalBERT**. The models are tested under two learning paradigms: **Zero-Shot Learning (ZSL)** and **Few-Shot Learning (FSL)**. The goal is to analyze and compare these models' performance in the context of disease prediction from unstructured text, particularly focusing on healthcare applications.

## Overview

The field of Natural Language Processing (NLP) has transformed the ability of machines to process, interpret, and extract meaningful insights from unstructured text. In the healthcare domain, disease prediction based on free-text symptom descriptions has become a promising tool for supporting clinical decision-making, especially in low-resource settings.

### The Models

1. **BART**: A general-purpose transformer model that excels in generative and comprehension tasks. Although pretrained on general corpora, it is evaluated in the healthcare domain without specific biomedical adaptation.
   
2. **BioBERT**: A variant of BERT pretrained on large biomedical datasets (e.g., PubMed, PMC), enabling it to leverage domain-specific knowledge for medical text classification tasks.
   
3. **BioClinicalBERT**: A further specialized version of BioBERT, pretrained on clinical notes and discharge summaries from the MIMIC-III database, capturing both biomedical and clinical language nuances.
   
4. **FLAN-T5**: A general-purpose instruction-tuned model capable of zero- and few-shot learning, offering robust generalization across various NLP tasks, including medical text classification.
   
5. **CNN**: A traditional convolutional neural network (CNN) model used as a baseline to evaluate the performance of modern transformer models in disease prediction tasks.

## Problem Setup

We examine disease prediction using two learning paradigms:

- **Zero-Shot Learning (ZSL)**: Evaluating model performance when no specific training examples are provided, simulating real-world applications where annotated data may be scarce.
  
- **Few-Shot Learning (FSL)**: Evaluating model performance with limited labeled data, which is often a constraint in clinical domains due to the high cost of data annotation.

The models are evaluated on four diverse medical datasets containing symptom-disease pairs and diagnostic labels.

## Key Findings

- **Domain-specific models (BioBERT and BioClinicalBERT)** consistently outperform general-purpose models (BART and FLAN-T5) across most datasets and learning setups.
  
- **BioClinicalBERT** excels in handling clinical language nuances, providing better performance in clinical settings than other models.
  
- **FLAN-T5** demonstrates strong generalization across various NLP tasks, though it lacks domain-specific adaptation.
  
- **CNN** serves as a useful baseline, allowing comparison with the more complex transformer models.


## Requirements

To run the code, ensure you have the following libraries installed:

```bash
pip install transformers datasets scikit-learn numpy torch
