---
title: "(NLP) Opinion Spam Detection using Machine Learning"
excerpt: "A study on classifying deceptive reviews using Naive Bayes, Logistic Regression, Decision Trees, and Random Forests"
tags: [OpinionSpam, TextClassification, NaturalLanguageProcessing, SupervisedLearning, FeatureEngineering, MachineLearning, DeceptionDetection]
collection: portfolio
---

## Project Overview

This project investigates methods for detecting deceptive hotel reviews, or opinion spam, using machine learning. The dataset includes both genuine and fake hotel reviews, with a focus on distinguishing between truthful and deceptive negative reviews. By improving the reliability of online reviews, this model seeks to address the problem of opinion spam, ultimately fostering more informed consumer decisions.

## The Data

The dataset consists of 800 hotel reviews divided equally into truthful and deceptive categories. Each category includes 400 positive and 400 negative reviews. The genuine reviews were sourced from popular online review sites, while the fake reviews were generated via Amazon Mechanical Turk. This analysis focuses on the 400 negative truthful and 400 negative deceptive reviews.

## Key Components

1. **Data Preprocessing**:
   - Text processing and normalization through TF-IDF vectorization.
   - Feature selection using both unigrams and bigrams to capture additional context.
   - Removal of sparse terms and stop words for optimized feature representation.

2. **Model Architectures**:
   - **Multinomial Naive Bayes**: A generative linear model.
   - **Logistic Regression with Lasso Penalty**: A discriminative linear model using L1 regularization for feature selection.
   - **Classification Trees**: Non-linear classifiers based on decision splits.
   - **Random Forests**: An ensemble of decision trees for robust classification.

3. **Training and Hyperparameter Tuning**:
   - Training conducted on Folds 1-4 (640 reviews) with Fold 5 (160 reviews) held out for testing.
   - Cross-validation and out-of-bag evaluation (for Random Forest) used for tuning key hyperparameters, such as:
      - Regularization parameter lambda for Logistic Regression.
      - Cost-complexity pruning parameter alpha for Decision Trees.
      - Number of trees and feature selection strategy for Random Forests.
      - Number of features for Multinomial Naive Bayes.

## Methodology

1. **Data Processing**:
   - **TF-IDF Vectorization**: Conversion of text into numerical vectors, followed by filtering of terms with low document frequency.
   - **Feature Engineering**: Use of unigrams and bigrams to enhance context and capture more complex relationships within the text.

2. **Model Comparison**:
   - Evaluation of both linear and non-linear models to assess classification performance.
   - Statistical tests to compare model accuracy between different approaches, with bigram and unigram features.

3. **Model Training and Evaluation**:
   - Model performance measured on the test fold using accuracy, precision, recall, and F1 score metrics.
   - Evaluation of selected models with and without bigrams to investigate the impact of feature granularity.

## Key Findings

1. **Model Comparisons**:
   - **Generative vs. Discriminative Linear Models**: Comparison of Multinomial Naive Bayes and Logistic Regression to determine which model more effectively captures text patterns in deceptive reviews.
   - **Impact of Non-Linear Models**: Analysis of whether Random Forests improve performance over linear models, given their capacity to capture complex interactions.
   - **Unigram vs. Bigram Features**: Testing of both feature types to evaluate whether bigrams improve classification performance.

2. **Top Features for Classification**:
   - Identification of the five most predictive terms for deceptive reviews and the five for genuine reviews, based on feature importance scores.

## Performance Metrics

The table below summarizes the performance of the four selected models (Multinomial Naive Bayes, Logistic Regression, Classification Trees, and Random Forests) with and without bigram features on the test set.

| Model (Bigram)       | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Naive Bayes          | 91.0%    | 88.2%     | 93.7%  | 90.9%    |
| Logistic Regression  | 86.3%    | 86.3%     | 86.3%  | 86.3%    |
| Decision Tree        | 61.8%    | 59.5%     | 73.7%  | 65.9%    |
| Random Forest        | 86.2%    | 81.5%     | 93.7%  | 87.2%    |

> Note: **Statistical Significance**: Statistical tests were conducted on model accuracy to determine if differences between models are significant.

## Technologies Used

Python, Scikit-learn, TF-IDF, GridSearchCV, Amazon Mechanical Turk

## Insights and Conclusions

- **Effectiveness of Feature Selection**: Multinomial Naive Bayes, with bigrams and feature selection, showed notable accuracy improvements in identifying deceptive reviews.
- **Comparative Model Performance**: Random Forests and Logistic Regression showed competitive accuracy, with significant improvements through tuning.
- **Feature Analysis**: Bigram features helped capture the nuanced phrasing patterns in deceptive reviews, while unigram features focused on individual word frequencies.

## Future Directions

Further exploration into deeper NLP models, such as Transformer-based models, could enhance accuracy in detecting complex deceptive patterns. Additionally, expanding feature engineering with advanced embeddings may capture even more subtle linguistic cues for opinion spam detection.

---

## Resources

- **Course**: Data Mining at Utrecht University
- **Referenced Studies**: Myle Ott et al., on opinion spam and review classification
---
