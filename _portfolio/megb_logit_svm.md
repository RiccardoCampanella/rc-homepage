---
title: "Handwritten Digit Classification using Logistic Regression and SVM"
excerpt: "A comparative analysis between logistic regression and SVM models for digit recognition tasks"
tags: [LogisticRegression, SVM, HandwrittenDigits, Classification, Sklearn, DataProcessing, HyperparameterTuning, ModelComparison, MachineLearning]
collection: portfolio
---

## Project Overview

This project aims to classify handwritten digits using two different machine learning models: Logistic Regression and Support Vector Machine (SVM). The goal is to assess the performance of each method in accurately identifying the digits from the well-known MNIST dataset.

## Key Components

1. **Data Preparation**:
   - Loading the MNIST dataset from `sklearn.datasets`
   - Splitting the data into training and testing sets
   - Normalizing feature values for improved model performance

2. **Model Architectures**:
   - Logistic Regression
   - Support Vector Machine (SVM) with different kernels (linear, RBF, polynomial)

3. **Hyperparameter Tuning**:
   - Logistic Regression: `penalty` and `C` values
   - SVM: `kernel`, `C`, `gamma`, and `degree` values
   - Grid search for optimal hyperparameters

## Methodology

1. **Logistic Regression**:
   - Standard implementation of multinomial logistic regression.
   - Hyperparameters like the regularization strength (`C`) were fine-tuned using cross-validation.
   - Achieved reasonable accuracy across different digits, but struggled with complex patterns compared to SVM.

2. **Support Vector Machine (SVM)**:
   - Multiple kernel functions were tested, including linear, RBF, and polynomial.
   - Hyperparameters such as `C` (penalty parameter), `gamma` (kernel coefficient), and `degree` (for polynomial kernels) were explored extensively.
   - RBF kernel performed particularly well, capturing nonlinear relationships that logistic regression couldn't.

## Comparison of Logistic Regression vs SVM

| Aspect               | Logistic Regression           | SVM (RBF Kernel)                   |
|----------------------|-------------------------------|------------------------------------|
| **Dimensionality**    | Linear separation             | Handles complex, nonlinear boundaries |
| **Performance**       | Moderate accuracy (~91%)      | Higher accuracy (~95%)             |
| **Hyperparameter Tuning** | Primarily `C`               | `C`, `gamma`, `kernel`             |
| **Computation Time**  | Faster training               | Slower, especially with RBF kernel |
| **Interpretability**  | Easier to interpret           | More complex due to kernel functions |
| **Best Use Case**     | Simple, linear relationships  | Nonlinear, complex patterns        |

## Model Training Results

1. **Logistic Regression**:
   - Achieved an accuracy of **91.1%** after tuning.
   - Struggled with complex digits like '3' and '5'.

2. **SVM**:
   - The best results came with the RBF kernel, achieving an accuracy of **95.6%**.
   - SVM showed superior performance in handling the nonlinearities present in handwritten digits.

3. **Confusion Matrix Analysis**:
   - Logistic Regression had more misclassifications for digits like '8' and '3'.
   - SVM's confusion matrix displayed fewer errors across most digits, with notable improvements in distinguishing between digits that appear similar.

## Technologies Used

- Python (NumPy, Matplotlib)
- Scikit-learn (Logistic Regression, SVM, GridSearchCV)
- Pandas for data handling
- Seaborn for visualization

## Conclusion

The comparison shows that SVM, particularly with the RBF kernel, outperforms logistic regression in the task of handwritten digit classification, especially when dealing with complex, nonlinear patterns. While logistic regression is faster and easier to interpret, SVM's ability to model more sophisticated relationships makes it the preferred choice for this dataset.

---
## Resources

- **Code Repository**: [GitHub - Handwritten Digit Classification](https://github.com/RiccardoCampanella/Pattern_Recognition)
- **Dataset**: MNIST from sklearn

---