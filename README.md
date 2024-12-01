# credit-risk-classification

## Overview of the Analysis
In this analysis, the primary goal was to evaluate the performance of a machine learning model in predicting the likelihood of loans being classified as either healthy (0) or high-risk (1). The dataset included financial information related to loans, such as borrower details and loan characteristics. The task was to predict the loan_status, which indicates whether a loan is classified as 0 (healthy) or 1 (high-risk).

The dependent variable, loan_status, was imbalanced, with a majority of loans being healthy. This was confirmed using value_counts to show the distribution of loan_status: the dataset contained 15,001 healthy loans and 507 high-risk loans. The analysis involved the following stages: data preprocessing (separating features and labels, splitting data into training and testing sets), fitting a logistic regression model, generating predictions, and evaluating model performance using a classification report and confusion matrix. The LogisticRegression algorithm was selected due to its simplicity and efficiency for binary classification tasks. Metrics such as accuracy, precision, recall, and F1-score were used to evaluate the model.

## Results
*Machine Learning Model 1 (Logistic Regression):
Accuracy: 99% overall accuracy.
Precision:
Class 0 (healthy loans): 1.00 (perfect precision).
Class 1 (high-risk loans): 0.86.
Recall:
Class 0 (healthy loans): 0.99.
Class 1 (high-risk loans): 0.94.
F1-Score:
Class 0: 1.00.
Class 1: 0.90.
