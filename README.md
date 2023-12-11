# Project credit-risk-classification

## Overview of the Analysis
In this analysis, the focus was on predicting loan status using historical lending data. The dataset, lending_data.csv, was read from the Resources folder and processed to create features (X) and labels (y). The data was split into training and testing sets using the train_test_split function. Loan Features include 
loan size, interest rate, borrower income, debt to income, num of accounts, derogatory marks, total debt. we need to predict loan status (0: Healthy Loan, 1: High-Risk Loan).

Machine Learning Process
Step 1: Split the Data into Training and Testing Sets
Data Loading:
The lending_data.csv data from the Resources folder was read into a Pandas DataFrame.
Data Splitting:
Labels (y) were created from the "loan_status" column.
Features (X) DataFrame was created from the remaining columns.
The data was split into training and testing datasets using train_test_split.

Step 2: Create a Logistic Regression Model with the Original Data
Model Training:
A logistic regression model was fitted using the training data (X_train and y_train).
Model Prediction and Evaluation:

Predictions were made on the testing data labels (X_test) using the fitted model.
The model's performance was evaluated using:
A confusion matrix.
Printing the classification report.

Methods Used
Logistic Regression, a commonly used classification algorithm, was selected for its interpretability and efficiency. The model's performance is evaluated using precision, recall, and accuracy metrics.

## Result
Precision and Recall Scores:
- Accuracy: 99%
- Precision (Class 0): 100%
- Precision (Class 1): 85%
- Recall (Class 0): 99%
- Recall (Class 1): 91%
- F1-Score (Class 0): 100%
- F1-Score (Class 1): 88%

## Summary
The logistic regression model demonstrated high accuracy and precision for predicting healthy loans (0), while also achieving a reasonable recall for high-risk loans (1). Precision for predicting high-risk loans is slightly lower, indicating some false positives. The choice of the model may depend on the specific problem and the associated costs of false positives and false negatives. 
If the primary concern is minimizing the risk associated with high-risk loans, the focus should be on achieving a high recall for class 1. This means identifying as many high-risk loans as possible, even if it results in some false positives (healthy loans being misclassified as high-risk). Therefore, I do not recommend this model.
Consequences of False Negatives: Missing a high-risk loan (false negative) could lead to financial losses or other negative consequences. Therefore, the model should be sensitive to the detection of high-risk cases.

