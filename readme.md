# Credit Risk Assessment for Consumer Loans

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![ML](https://img.shields.io/badge/Machine%20Learning-Classification-orange)]()

## 📌 Overview

This project addresses a core challenge for financial institutions: **credit risk assessment**. With the French consumer credit market exceeding €180 billion, accurate predictive models are essential to optimize loan approval decisions while minimizing default risk.

We implement and compare **five machine learning classification algorithms** to predict payment defaults. The goal is to find the right balance between accepting solvent borrowers (maximizing revenue) and rejecting high-risk profiles (limiting losses), all while maintaining regulatory compliance through model explainability.

---

## 🎯 Business Context

| Aspect | Description |
|--------|-------------|
| **Industry** | Banking / Financial Services |
| **Market** | French consumer credit (€180B+) |
| **Key trade-off** | Maximize revenue vs. limit default losses |
| **Constraint** | Decisions must be explainable (regulatory compliance like GDPR, Basel) |

---

## 📊 Dataset Description

The anonymized dataset contains the following features for each borrower:

| Variable | Description | Type |
|----------|-------------|------|
| `revenu` | Monthly income (€) | Numeric |
| `depnais` | Department of birth | Categorical |
| `datenaiss` | Date of birth | Date |
| `durée_crédit` | Loan duration (months) | Numeric |
| `montcred` | Loan amount (€) | Numeric |
| `situfam` | Family situation (0 = single, 1 = couple) | Binary |
| `ancienneté` | Professional seniority (years) | Numeric |
| `cb` | Has credit card? (0 = no, 1 = yes) | Binary |
| `incident` | Payment default? (0 = no, 1 = yes) | **Target Variable** |

> **Note**: Data has been pre-cleaned and is ready for analysis.

---

## 🧪 Methodology

### Part 1: Preprocessing & Exploratory Analysis
- Calculate borrower age from date of birth
- Group departments into administrative regions (dimensionality reduction)
- Generate descriptive statistics and visualizations

### Part 2: Model Comparison

We implement and evaluate five classification algorithms:

| Algorithm | Key Characteristics | Interpretability |
|-----------|---------------------|-------------------|
| **Decision Tree** | Rule-based hierarchical structure | ⭐⭐⭐⭐⭐ |
| **Random Forest** | Ensemble of trees, robust | ⭐⭐⭐ |
| **k-NN** | Similarity-based, instance-based | ⭐⭐ |
| **Naive Bayes** | Probabilistic, efficient | ⭐⭐⭐⭐ |
| **MLP (Neural Network)** | Non-linear relationships | ⭐ |

**Validation Protocol**:
- Train/Test split: **70% / 30%**
- Final evaluation on test set only (no data leakage)

### Part 3: Interpretability Analysis
- Identify the most discriminative features
- Assess how to justify a decision to a client (regulatory perspective)

### Part 4: Performance Metrics
- Confusion matrix
- Accuracy
- Precision & Recall (focus on default prediction)

---

## 📁 Repository Structure
