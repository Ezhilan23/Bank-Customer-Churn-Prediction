# Bank Customer Churn Prediction

## Project Overview

This project aims to predict customer churn for a European multinational bank operating in France, Germany, and Spain. Using machine learning, we analyze which customers are most likely to leave the bank, allowing the organization to take proactive steps to retain them. The dataset includes demographic, financial, and behavioral attributes of customers.

---

## Dataset

The dataset contains the following key features:

- **Demographics**: Geography, Gender, Age, Tenure
- **Financial Info**: Credit Score, Balance, Estimated Salary
- **Customer Behavior**: Number of Products, HasCrCard, IsActiveMember
- **Target**: `Exited` (1 = churned, 0 = retained)

---

## Problem Statement

**"Can we predict whether a customer will churn based on their profile and activity with the bank?"**

---

## Methodology

### Exploratory Data Analysis (EDA)

- Identified correlations between churn and features like geography, activity level, and balance.
- Discovered imbalance in churn classes (~20% churned).

### Data Preprocessing

- Handled nulls, outliers, and duplicates
- Encoded categorical variables (e.g., Geography, Gender)
- Applied SMOTE to balance the dataset
- Scaled features for optimal model performance

### Model Development

Trained and evaluated the following classifiers:

- Logistic Regression (LR)
- Naive Bayes (NB)
- Random Forest (RF)
- XGBoost
- AdaBoost
- CART (Decision Tree)
- K-Nearest Neighbors (KNN)

---

## Model Performance

| Model     | Recall (Test) | F1 Score (Test) | AUROC (Test) | Precision (Test) |
|-----------|---------------|-----------------|---------------|------------------|
| LR        | 1.000000      | 0.999500        | 0.999686      | 0.997555         |
| NB        | 1.000000      | 0.999500        | 0.999686      | 0.997555         |
| RF        | 1.000000      | 0.999001        | 0.999372      | 0.995122         |
| XGBoost   | 1.000000      | 0.999001        | 0.999372      | 0.995122         |
| AdaBoost  | 1.000000      | 0.999500        | 0.999686      | 0.997555         |
| CART      | 0.995098      | 0.998000        | 0.996921      | 0.995098         |
| KNN       | 0.975490      | 0.990000        | 0.984604      | 0.975490         |

---

## Key Insights

- All models achieved high scores, with **Logistic Regression**, **Naive Bayes**, and **AdaBoost** yielding perfect recall on the test set.
- **XGBoost** and **Random Forest** demonstrated excellent overall balance in precision, recall, and F1-score.
- Features such as **Geography**, **Balance**, and **IsActiveMember** significantly influenced churn prediction.
- SMOTE proved effective in balancing the minority class and boosting model generalization.

---

## Conclusion

The project successfully demonstrates that machine learning can accurately predict bank customer churn. With models like **Random Forest** and **XGBoost**, banks can identify at-risk customers with high precision and recall, enabling targeted retention strategies and improved customer satisfaction.

---

## Future Work

- Fine-tune model hyperparameters for better recall–precision balance
- Deploy model as a REST API or web application
- Integrate real-time customer behavior data for dynamic churn prediction
- Create dashboards for business users to monitor churn risk

---

