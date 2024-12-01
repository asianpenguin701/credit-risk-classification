# credit-risk-classification

## Overview of the Analysis
In this analysis, the primary goal was to evaluate the performance of a machine learning model in predicting the likelihood of loans being classified as either healthy (0) or high-risk (1). The dataset included financial information related to loans, such as borrower details and loan characteristics. The task was to predict the loan_status, which indicates whether a loan is classified as 0 (healthy) or 1 (high-risk).

The dependent variable, loan_status, was imbalanced, with a majority of loans being healthy. This was confirmed using value_counts to show the distribution of loan_status: the dataset contained 15,001 healthy loans and 507 high-risk loans. The analysis involved the following stages: data preprocessing (separating features and labels, splitting data into training and testing sets), fitting a logistic regression model, generating predictions, and evaluating model performance using a classification report and confusion matrix. The LogisticRegression algorithm was selected due to its simplicity and efficiency for binary classification tasks. Metrics such as accuracy, precision, recall, and F1-score were used to evaluate the model.

## Results
### Machine Learning Model 1:

| Metric           | Class 0 (Healthy Loans) | Class 1 (High-Risk Loans) | Overall  |
|-------------------|--------------------------|---------------------------|----------|
| **Accuracy**      |                          |                           | **99%**  |
| **Precision**     | 1.00 (Perfect Precision) | 0.86                      |          |
| **Recall**        | 0.99                     | 0.94                      |          |
| **F1-Score**      | 1.00                     | 0.90                      |          |

- **Accuracy**:
  - Overall accuracy: **99%**.
  - This means the model correctly predicts the loan status for 99% of the cases.

- **Precision**:
  - Class 0 (Healthy Loans): **1.00** → Perfect precision, indicating no false positives.
  - Class 1 (High-Risk Loans): **0.86** → 86% of predicted high-risk loans are actually high-risk.

- **Recall**:
  - Class 0 (Healthy Loans): **0.99** → The model identifies 99% of all healthy loans correctly.
  - Class 1 (High-Risk Loans): **0.94** → The model identifies 94% of all high-risk loans correctly.

- **F1-Score**:
  - Class 0 (Healthy Loans): **1.00** → Perfect balance between precision and recall.
  - Class 1 (High-Risk Loans): **0.90** → Indicates good overall performance for high-risk loans.

## Summary
The logistic regression model seems to perform best for predicting healthy loans (Class 0), as it achieves perfect precision (1.00) and F1-score (1.00), along with a recall of 0.99. This indicates that the model is highly reliable in identifying and predicting healthy loans without any false positives.<br/>

However, the model also performs well for high-risk loans (Class 1), achieving a strong recall of 0.94 and an F1-score of 0.90, although its precision for Class 1 is slightly lower at 0.86, indicating some false positives.

Performance depends on the problem we are trying to solve:

* If the goal is to minimize false negatives (i.e., failing to identify high-risk loans), the model's high recall for Class 1 (0.94) makes it effective for identifying risky loans.
* If minimizing false positives (i.e., incorrectly classifying healthy loans as high-risk) is more critical, the model performs better for Class 0, where it achieves perfect precision.

Overall, this model is recommended for tasks prioritizing balanced performance, with a slight emphasis on identifying high-risk loans, as it maintains high recall and accuracy across both classes. If further optimization is needed for high-risk loans, techniques like class rebalancing or adjusting thresholds could be explored.

