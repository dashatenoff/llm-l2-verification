# Semantic Feature Verification for LLM-Based Pricing Models

Research implementation for the paper:

**"The Impact of Two-Level Hallucination Filtering in Large Language Models on Machine Learning Performance in Feature Extraction from Text Data"**

## Overview

This project investigates how semantic verification of LLM-generated attributes affects the quality of machine learning models in e-commerce pricing tasks.

The proposed pipeline combines:

- LLM-based feature extraction;
- L1 syntactic filtering (Exact Match);
- L2 semantic verification using Natural Language Inference (NLI);
- CatBoost regression for price prediction.

The architecture is designed to reduce hallucinated attributes while preserving semantically grounded features extracted from unstructured product descriptions.

## Pipeline

Raw Text → LLM Extraction → L1 Filter → L2 NLI Verification → Verified Features → CatBoost Regression

## Main Results

- R² improved from **0.056** to **0.303**
- Up to **40%** of valid features were recovered after L1 rejection
- Verified attributes significantly improved feature interpretability

## Technologies

- Python
- CatBoost
- Llama 3
- DeBERTa-v3
- HuggingFace Datasets
- Scikit-learn

## Repository Structure

```text
├── notebooks/
├── figures/
├── results/
├── README.md
└── requirements.txt
