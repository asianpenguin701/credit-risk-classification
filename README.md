# credit-risk-classification

## Overview of the Analysis
In this analysis, the primary goal was to evaluate the performance of a machine learning model in predicting the likelihood of loans being classified as either healthy (0) or high-risk (1). The dataset included financial information related to loans, such as borrower details and loan characteristics. The task was to predict the loan_status, which indicates whether a loan is classified as 0 (healthy) or 1 (high-risk).

The dependent variable, loan_status, was imbalanced, with a majority of loans being healthy. This was confirmed using value_counts to show the distribution of loan_status: the dataset contained 15,001 healthy loans and 507 high-risk loans. The analysis involved the following stages: data preprocessing (separating features and labels, splitting data into training and testing sets), fitting a logistic regression model, generating predictions, and evaluating model performance using a classification report and confusion matrix. The LogisticRegression algorithm was selected due to its simplicity and efficiency for binary classification tasks. Metrics such as accuracy, precision, recall, and F1-score were used to evaluate the model.

## Results
Accuracy:
* 99% overall accuracy<br />
Precision<br />
* Class 0 (healthy loans): 1.00 (perfect precision)
* Class 1 (high-risk loans): 0.86
Recall:</br>
* Class 0 (healthy loans): 0.99</br>
* Class 1 (high-risk loans): 0.94</br>
F1-Score:</br>
* Class 0: 1.00</br>
* Class 1: 0.90

- **Class 0 (Healthy Loans)**:
  - Recall: **0.99** → The model correctly identifies 99% of all healthy loans.
- **Class 1 (High-Risk Loans)**:
  - Recall: **0.94** → The model correctly identifies 94% of all high-risk loans.

## Summary
The logistic regression model performed exceptionally well, achieving high accuracy and strong metrics across both loan classes. It performed best for predicting healthy loans (0), with perfect precision and near-perfect recall. For high-risk loans (1), while precision was slightly lower (0.86), the model demonstrated strong recall (0.94), which is critical for identifying risky loans.

The model is recommended for use, particularly if the primary goal is to minimize false negatives (failing to identify high-risk loans). However, if reducing false positives (incorrectly labeling healthy loans as high-risk) is more important, additional techniques like adjusting class weights or using a more complex model might improve precision for class 1. Overall, the logistic regression model balances simplicity with excellent performance, making it suitable for this task.
