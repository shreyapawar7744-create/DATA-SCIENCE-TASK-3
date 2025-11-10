# DATA-SCIENCE-TASK-3
This document details the machine learning workflow for Task 3, which involved predicting customer subscription to a term deposit (y variable) using a Decision Tree Classifier on the Bank Marketing dataset.

This is the description for Task 3 (Bank Marketing Dataset - Decision Tree Classification), presented in a clear, continuous text format.
The objective of Task 3 was to develop a predictive model for a bank marketing campaign using a Decision Tree Classifier. The goal was to predict whether a customer would subscribe to a term deposit, represented by the target variable y.

# Data Preparation
The analysis began with the Bank Marketing dataset (bank-additional.csv), which contained 4,119 entries and 21 columns. A preliminary data quality check confirmed that the dataset was remarkably clean, with zero missing values across all 21 features, thus eliminating the need for imputation . Since the Decision Tree algorithm operates on numerical data, all categorical features (columns with object data type) were converted into numerical representations using Label Encoding . Finally, the data was partitioned into training and testing sets using an 80/20 ratio (test_size=0.2) for model development and evaluation.

# Model Training and Evaluation
A Decision Tree Classifier was chosen for the classification task. The model was trained using the entropy criterion for calculating information gain and was intentionally limited to a maximum depth of 5 (max_depth=5) to prevent overfitting and maintain interpretability .
The model's performance was assessed on the test set, yielding an overall Accuracy of 0.9029 (approximately 90.29%).

#The Classification Report provided a more granular view of performance, particularly for the positive class (Class 1: subscribed 'yes'):
Precision (Class 1): 0.58 
Recall (Class 1): 0.48 
F1-Score (Class 1): 0.52 
The Confusion Matrix further detailed the classification results: 700 true negatives (correctly predicted 'no subscription') and 44 true positives (correctly predicted 'yes subscription'). The relatively lower scores for the positive class (Class 1) indicate the model had more difficulty correctly identifying actual subscribers.

# Feature Importance
Analysis of the trained model identified the features that contributed most significantly to the prediction:
duration (The duration of the last contact)
nr.employed (Number of employees, a socio-economic indicator)
emp.var.rate (Employment variation rate, a socio-economic indicator)
These findings suggest that contact duration and prevailing macroeconomic factors were the strongest drivers for predicting a customer's subscription decision.
