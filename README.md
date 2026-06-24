# Explainable AI for Lung Cancer Survival Prediction

## Overview

This repository contains the implementation of the research paper:

**"Explainable AI Identifies Key Determinants of Survival in Lung Cancer Across Multiple Predictive Frameworks"**

The study compares three survival analysis frameworks for lung adenocarcinoma (LUAD) prognosis:

* Random Survival Forest (RSF)
* Cox Proportional Hazards (CPH)
* DeepSurv

To improve interpretability and clinical trust, SHAP (SHapley Additive exPlanations) is used to identify the most influential prognostic factors affecting patient survival.

---

## Research Objective

Lung cancer remains one of the leading causes of cancer-related mortality worldwide. Accurate survival prediction can support:

* Clinical decision-making
* Risk stratification
* Personalized treatment planning
* Prognostic assessment

This project evaluates and explains multiple survival prediction models using a unified experimental framework.

---

## Dataset

The study uses the Lung Adenocarcinoma (LUAD) clinical dataset obtained from The Cancer Genome Atlas (TCGA).

### Data Processing

The preprocessing pipeline includes:

* Train-test split (75%-25%)
* Median imputation for missing values
* IQR-based outlier clipping
* Label encoding for categorical variables
* Feature engineering based on clinical knowledge

---

## Feature Set

### Clinical Features

* Age
* Tumor Purity
* Tumor Stage (T)
* Lymph Node Stage (N)
* Metastasis Stage (M)
* Tumor Burden Score
* Metastasis Flag
* Lymph Node Flag

### Interaction Features

* Age × Tumor Stage
* Age × Lymph Node Stage
* TN Interaction
* Tumor Purity × Tumor Stage

### Additional Deep Learning Feature

* Age²

---

## Models Implemented

### 1. Cox Proportional Hazards (CPH)

Classical survival analysis model that estimates hazard ratios and provides interpretable risk estimation.

### 2. Random Survival Forest (RSF)

Ensemble-based survival model capable of capturing nonlinear interactions and complex feature relationships.

### 3. DeepSurv

Deep neural network adaptation of the Cox model designed to learn nonlinear survival patterns from clinical data.

---

## Explainability

SHAP (SHapley Additive exPlanations) is used to:

* Interpret model predictions
* Quantify feature importance
* Analyze global survival determinants
* Improve model transparency

---

## Results

| Model                    | Concordance Index (C-Index) |
| ------------------------ | --------------------------- |
| Random Survival Forest   | 0.6335                      |
| Cox Proportional Hazards | 0.6102                      |
| DeepSurv                 | 0.6022                      |

### Key Findings

Across all three models, the most influential survival predictors were:

* Tumor Stage
* Lymph Node Involvement
* Metastatic Status
* Patient Age
* Tumor Burden

The consistency of feature rankings across different modeling paradigms indicates robust and clinically meaningful prognostic signals.



## Technologies Used

* Python
* Scikit-Learn
* Lifelines
* Scikit-Survival
* PyTorch
* SHAP
* Pandas
* NumPy
* Matplotlib

---

## Research Contribution

This work provides:

* A unified comparison of classical, ensemble, and deep survival models
* Consistent preprocessing and evaluation across all frameworks
* Cross-model explainability using SHAP
* Identification of clinically relevant prognostic factors for lung adenocarcinoma survival prediction

---

## Citation

If you use this work, please cite:

Muhammad Ibrahim Saeed, Nabeela Kausar.

"Explainable AI Identifies Key Determinants of Survival in Lung Cancer Across Multiple Predictive Frameworks."

---

## Author

Muhammad Ibrahim Saeed

AI Engineer | Machine Learning | NLP | Retrieval-Augmented Generation (RAG)

LinkedIn: www.linkedin.com/in/muhammad-ibrahim-a787142bb
