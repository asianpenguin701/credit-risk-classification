# credit-risk-classification

## Overview of the Analysis
The purpose of this analysis was to evaluate a machine learning model for predicting loan status as either healthy (Class 0) or high-risk (Class 1), using financial data related to borrower characteristics and loan details. The target variable, loan_status, was imbalanced, with 15,001 healthy loans and 507 high-risk loans. The analysis involved splitting the data into features and labels, followed by training a Logistic Regression model on the training data. The model's performance was evaluated using metrics such as accuracy, precision, recall, and F1-score. The model achieved excellent accuracy (99%) and performed exceptionally well for healthy loans, with perfect precision and F1-score, while also maintaining strong recall (0.94) and F1-score (0.90) for high-risk loans. This process highlights the model's effectiveness as a baseline for loan risk prediction, with potential for further optimization based on specific goals.

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
The logistic regression model seems to perform best for predicting healthy loans (Class 0), as it achieves perfect precision (1.00) and F1-score (1.00), along with a recall of 0.99. This indicates that the model is highly reliable in identifying and predicting healthy loans without any false positives.

However, the model also performs well for high-risk loans (Class 1), achieving a strong recall of 0.94 and an F1-score of 0.90, although its precision for Class 1 is slightly lower at 0.86, indicating some false positives.

Overall, this model is recommended for tasks prioritizing balanced performance, with a slight emphasis on identifying high-risk loans, as it maintains high recall and accuracy across both classes. If further optimization is needed for high-risk loans, other techniques could be explored.

