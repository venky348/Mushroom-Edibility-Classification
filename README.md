# Mushroom Edibility Classification

This project focuses on classifying mushrooms as edible or poisonous using machine learning models. The dataset includes various physical and environmental attributes of mushrooms and aims to develop robust classification models to ensure accurate predictions.

---

## Overview

The repository includes:
- Data preprocessing and exploratory data analysis (EDA) to identify patterns and relationships.
- Implementation of machine learning models:
  - **Logistic Regression (Softmax Regression)**
  - **Support Vector Machine (SVM)**
  - **Random Forest Classifier**
  - **Ensemble Voting Classifier**
- Comparison of model performance in training, validation, and testing phases.

---

## Dataset Details

- **Number of Entries:** 2,702 (sampled from the original dataset)
- **Number of Columns:** 9
- **Features:**
  - Cap Diameter, Cap Shape, Gill Attachment, Gill Color, Stem Height, Stem Width, Stem Color, Season.
- **Target Variable:**
  - `Class` (Edible: 0, Poisonous: 1)

---

## Key Insights from Data Analysis

1. **Distributions:**
   - Most features are right-skewed or have uniform distributions, indicating discrete or categorical nature.
   - The target variable (`Class`) exhibits a bimodal distribution, highlighting distinct categories.

2. **Correlation Analysis:**
   - Strong positive correlations between Cap Diameter and Stem Width.
   - Moderate correlations for features like Cap Shape and Gill Attachment.

3. **Potential Patterns:**
   - Overlap in features like Stem Height and Cap Diameter across classes suggests no single feature is sufficient for classification, emphasizing the need for combined features.

---

## Machine Learning Models

### 1. Logistic Regression (Softmax)
- **Best Hyperparameters:**
  - Regularization (C): 1
  - Solver: Newton-CG
  - Max Iterations: 100
- **Test Accuracy:** 65.80%

### 2. Support Vector Machine (SVM)
- **Best Hyperparameters:**
  - C: 100
  - Kernel: RBF
  - Degree: 2
  - Gamma: Scale
- **Test Accuracy:** 89.65%

### 3. Random Forest Classifier
- **Best Hyperparameters:**
  - Number of Trees: 200
  - Max Depth: None
  - Min Samples Split: 2
  - Min Samples Leaf: 1
- **Test Accuracy:** 95.19%

### 4. Ensemble Voting Classifier
- Combines predictions from Logistic Regression, SVM, and Random Forest models.
- **Test Accuracy:** 91.13%

---

## Model Performance Summary

| Model                         | Training Accuracy | Validation Accuracy | Test Accuracy |
|-------------------------------|-------------------|---------------------|---------------|
| Logistic Regression (Softmax) | 65.56%           | 62.48%             | 65.80%        |
| Support Vector Machine (SVM)  | 90.99%           | 87.43%             | 89.65%        |
| Random Forest Classifier       | 100.00%          | 94.45%             | 95.19%        |
| Voting Classifier (Soft)       | 97.35%           | 89.46%             | 91.13%        |

---

## Conclusion

The **Ensemble Voting Classifier** emerged as the most balanced model, providing strong performance across all datasets. While the Random Forest Classifier achieved the highest accuracy, its potential overfitting makes the Voting Classifier more reliable for generalization.

This project demonstrates the value of combining classifiers to enhance robustness and achieve consistent results, especially for datasets with overlapping features.

---

