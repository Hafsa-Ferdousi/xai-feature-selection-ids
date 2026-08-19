# Explainable Hybrid Feature Selection for Network Intrusion Detection

An explainable hybrid feature-selection framework for multiclass Network Intrusion Detection Systems (NIDS), evaluated on the **CIC-IDS2017** and **CSE-CIC-IDS2018** benchmark datasets.

---

## Overview

Network intrusion detection datasets contain a large number of traffic features, many of which may be redundant, irrelevant, or highly correlated. This high dimensionality can increase computational cost, reduce model interpretability, and negatively affect model generalization.

This research proposes an **explainable hybrid feature-selection framework** that combines multiple feature-selection strategies to identify informative network traffic features while maintaining competitive classification performance.

The research investigates:

- High-dimensional network traffic data
- Redundant and correlated features
- Multiclass intrusion detection
- Feature-selection effectiveness
- Model performance before and after feature selection
- Explainability of selected features
- Cross-dataset generalization

---

## Research Objectives

The main objectives of this study are:

1. Preprocess and standardize network intrusion datasets.
2. Establish baseline performance using the complete feature set.
3. Investigate correlation-based feature selection.
4. Apply Boruta-based feature selection.
5. Develop and evaluate a hybrid feature-selection strategy.
6. Compare classification performance using selected and non-selected features.
7. Analyze feature importance and model explanations.
8. Evaluate generalization through cross-dataset validation.

---

## Datasets

This study uses two benchmark network intrusion detection datasets:

### CIC-IDS2017

The CIC-IDS2017 dataset contains realistic network traffic representing benign activities and multiple types of attacks.

### CSE-CIC-IDS2018

The CSE-CIC-IDS2018 dataset provides a diverse collection of network traffic and attack scenarios.

> **Note:** The original datasets are not included in this repository because of their large size. Please download the datasets from their official sources.

---

## Methodology

The overall research pipeline is:

```text
Raw Network Traffic
        │
        ▼
Data Preprocessing
        │
        ├── Missing-value handling
        ├── Duplicate removal
        ├── Label encoding
        ├── Data cleaning
        │
        ▼
Baseline Model
        │
        │ Full Feature Set
        ▼
Feature Selection
        │
        ├── Correlation-based Selection
        ├── Boruta Selection
        └── Hybrid Feature Selection
        │
        ▼
Model Training
        │
        ├── Random Forest
        ├── XGBoost
        ├── LightGBM
        └── CatBoost
        │
        ▼
Evaluation
        │
        ├── Accuracy
        ├── Precision
        ├── Recall
        ├── F1-score
        └── Confusion Matrix
        │
        ▼
Explainable AI
        │
        ├── Feature Importance
        └── SHAP & LIME Analysis
        │
        ▼
Cross-Dataset Validation
