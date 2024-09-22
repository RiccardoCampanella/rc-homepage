---
title: "Explainability in Machine Learning: A Study on Personality Predictions"
excerpt: "Exploring various models for job interview invitation predictions using explainability techniques"
tags: [MachineLearning, PersonalityPrediction, Explainability, JobInterviews, LinearModels, XGBoost, DataProcessing, ModelInterpretation]
collection: portfolio
---


## Project Overview

This project aims to apply explainability techniques to predict job interview invitations based on personality scores from the ChaLearn LAP-FI dataset. The goal is to explore different machine learning models and analyze their interpretability to provide insights into model behavior and decision-making processes.

## Key Components
1. **Data Preparation**:
   - Reading data from the ChaLearn LAP-FI dataset
   - Features: BIG-5 personality traits (openness, extraversion, conscientiousness, neuroticism, agreeableness)
   - Target variable: job interview invitation
2. **Model Architectures**:
   - Linear Regression
   - Explainable Boosting Machine
   - One-layer Neural Network Regressor (MLP)
3. **Training Approaches**:
   - Train-validation split for model evaluation
   - Cross-validation for parameter tuning
   - Feature importance analysis

## Methodology
1. **Data Preprocessing**:
   - Handling missing values
   - Normalizing numerical data
   - Train-test split for model evaluation
2. **Explainability Techniques**:
   - **PDP**: Partial dependence plots for understanding global model behavior, showing how a feature affects predictions on average across the dataset.
   - **ICE**: Individual Conditional Expectation plots display how a feature influences the prediction for individual data points, allowing analysis of interactions and variability across instances.
   - **PFI**: Permutation Feature Importance estimates the importance of a feature by randomly permuting its values and measuring the drop in model performance, helping to identify key predictors.
3. **Model Evaluation**:
   - Assessing models based on accuracy and interpretability
   - Comparison between linear and complex models

## Advantages of Explainability in Personality Prediction
- Provides insight into model decision-making
- Highlights important features driving predictions
- Helps build trust in AI systems used for high-stakes decisions
- Supports fairness by detecting biases in the model

## Comparison of Explainability: Linear Regression vs NNs
- Linear regression offers strong interpretability, especially for understanding the influence of individual features. In this dataset, it provided clear insights into the importance of personality traits for predicting job interview invitations. The model explained over 91% of the variance (R² > 0.91), with conscientiousness being the most significant feature. Moreover, t-statistics and p-values confirmed the significance of all coefficients, indicating robust feature contributions. This makes linear regression ideal for global model interpretability, where one can directly quantify the impact of each feature on the outcome.

- On the other hand, neural networks (NNs) like the multi-layer perceptron (MLP) offer competitive performance but at the cost of lower interpretability. In this case, an MLP achieved a root mean square error (RMSE) of 0.043 on the development set, showing its effectiveness in prediction. However, NNs are often seen as "black boxes," where it becomes difficult to understand how individual features influence the model's decisions.

- To address this, explainability techniques such as Permutation Feature Importance (PFI) and Individual Conditional Expectation (ICE) were used to analyze the neural network. These techniques helped uncover the importance of personality traits like openness and conscientiousness in the model's predictions, revealing that the NN heavily relied on these features. While this adds some interpretability, it is still less intuitive than linear regression.

## Comparison of Interpretability Methods

| **Method**                        | **Description**                                                                 | **Advantages**                                                                                             | **Limitations**                                                                 |
|------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| **Linear Regression**              | A simple model that estimates relationships between features and the target variable.                          | - Easy to interpret coefficients <br> - Provides global model insights (R², p-values)                      | - Limited to linear relationships <br> - Struggles with complex patterns        |
| **Permutation Feature Importance (PFI)** | Measures feature importance by observing the change in model performance after permuting feature values.        | - Model-agnostic <br> - Captures global importance                                                           | - Computationally expensive <br> - Can be misleading if features are correlated |
| **Individual Conditional Expectation (ICE)** | Plots show how changing one feature affects individual predictions.                                              | - Provides insight into individual feature effects <br> - Captures variability across instances              | - Harder to interpret for larger datasets <br> - Does not account for interactions with other features |
| **Partial Dependence Plots (PDP)** | Visualizes the average effect of a feature on predictions by marginalizing over the other features.              | - Offers global insight into feature influence <br> - Useful for identifying non-linear relationships        | - Assumes feature independence <br> - Can obscure individual variability       |

## Libraries Used
Python, Graphviz, Matplotlib, Pandas, Statsmodels, Scikit-learn

---
## Resources
- **Code Repository**: [GitHub - XAI](https://github.com/RiccardoCampanella/XAI)
- **Course**:  Human-centered Machine Learning, Utrecht University
- **Dataset Paper**: [ChaLearn LAP-FI Dataset](https://ieeexplore.ieee.org/abstract/document/7966041)
---