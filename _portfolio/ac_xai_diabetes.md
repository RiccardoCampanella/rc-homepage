---
title: "(XAI) Explaining Readmission of Diabetes Patients"
excerpt: "Analyzing factors contributing to diabetes patient readmissions using various explainable AI techniques"
tags: [MachineLearning, ExplainableAI, HealthcareAnalytics, DiabetesReadmission, RuleFit, BayesianNetworks, ExplainableBoostingMachine, NeuralNetworks, SHAP]
collection: portfolio
---

## Project Overview

This project aims to identify and analyze factors contributing to the readmission of diabetes patients using various explainable machine learning methods. The study focuses on two main questions:

1. What factors contribute most over time to a diabetes patient being readmitted?
2. What general features influence readmission risk in diabetic patients?

## Project Poster

[![Project Poster](https://riccardocampanella.github.io/rc-homepage/images/Diabetes_Research_poster.jpg)](https://riccardocampanella.github.io/rc-homepage/files/Diabetes_Research_poster.pdfDiabetes_Research_poster.pdf)

[Download Project Poster (PDF)](https://riccardocampanella.github.io/rc-homepage/files/Diabetes_Research_poster.pdfDiabetes_Research_poster.pdf)

## Key Components

1. **Data Preprocessing**:
   - Removal of features with >50% missing values
   - Sorting datapoints by patient number and encounter ID
   - Mapping of diagnostic codes to ICD9 descriptions
   - Feature filtering based on importance scores

2. **Machine Learning Models**:
   - RuleFit
   - Bayesian Networks (Tree Augmented Naive Bayes and Forest Augmented Naive Bayes)
   - Explainable Boosting Machine (EBM)
   - Neural Network with SHAP analysis

3. **Explainability Techniques**:
   - Rule extraction (RuleFit)
   - Causal tree construction (Bayesian Networks)
   - Global and local explanations (EBM)
   - SHAP (SHapley Additive exPlanations) analysis

## Model Performance Comparison

| Model | Accuracy | F1-score (<30 days) | F1-score (>30 days) | F1-score (No Readmission) |
|-------|----------|---------------------|---------------------|---------------------------|
| RuleFit (Filtered) | 0.58 | 0.01 | 0.31 | 0.71 |
| RuleFit (Unfiltered) | 0.57 | 0.01 | 0.33 | 0.71 |
| TANBS | 0.555 | - | - | - |
| FANBS | 0.616 | - | - | - |
| EBM | 0.58 | 0.06 | 0.40 | 0.70 |
| Neural Network (Filtered) | 0.573 | 0.03 | 0.36 | 0.71 |
| Neural Network (Unfiltered) | 0.573 | 0.02 | 0.44 | 0.71 |

## Key Findings

1. The most important features for predicting readmission include:
   - Number of inpatient visits
   - Discharge disposition ID
   - Number of diagnoses
   - Admission source ID
   - Diabetes medication

2. All models struggled with accurately predicting readmissions within 30 days, highlighting the complexity of short-term risk factors.

3. The integration of multiple explainable AI techniques provided comprehensive insights into both temporal and causal relationships affecting readmission risk.

## Ethical Considerations

- Ensuring patient privacy and data security
- Obtaining informed consent for data usage
- Evaluating models for fairness across patient groups
- Clinical validation before deployment

## Resources

- **Data Source**: Diabetes 130-US Hospitals for Years 1999-2008 dataset
- **Libraries Used**: TensorFlow, Keras, SHAP, H2O, pgmpy, interpret.glassbox
- **Code Repository**: [GitHub - XAI DIabetes Readmission](https://github.com/TaherJarUU/HCML-Project/blob/main/BN_important_features_experiment.ipynb)

---