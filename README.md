Loan Approval Prediction System

This repository contains a machine learning project that builds, evaluates, and compares classification models to predict whether a loan application will be approved or rejected. The project includes data preprocessing, handling missing values, addressing class imbalance with SMOTE, training multiple classifiers, evaluating performance, visualizing results, and saving the trained model.

Dataset Source

Kaggle – Loan Approval Prediction Dataset

Description: Financial and personal details of loan applicants, including income, assets, liabilities, credit score, and more.

Target: Predict whether a loan application will be approved (1) or rejected (0)

Models Compared

Decision Tree Classifier (Baseline)

Trained on original (imbalanced) data

High accuracy without resampling

Interpretable and easy to implement

Logistic Regression

Compared after SMOTE balancing

Linear baseline for classification

Lower performance on imbalanced data

Decision Tree (After SMOTE)

Trained on balanced dataset using SMOTE

Outperformed logistic regression significantly

Features

Data loading and exploration

Handling missing values using median and mode

Label encoding for categorical features

Stratified train-test split

SMOTE oversampling for class imbalance

Model training and evaluation including:

Precision, Recall, F1-score

Confusion Matrix

ROC Curve and AUC

Model saving with joblib

Sample Results

Before SMOTE (Baseline Model: Decision Tree)

Metric	Class 0 	 Class 1
Precision	0.97	   0.98
Recall	0.99	     0.96
F1-Score	0.98	   0.97
Accuracy	0.98	

Very strong performance even without balancing

After SMOTE (Balanced Training Data)

Model	Accuracy	F1 Score (Class 1)
Decision Tree	0.98	0.97
Logistic Regression	0.81	0.75

Decision Tree remained superior after balancing
Logistic Regression underperformed due to data complexity

Requirements

pandas

numpy

scikit-learn

imbalanced-learn

matplotlib

seaborn

joblib

Result Summary

The baseline Decision Tree performed well on the original data (98 percent accuracy)

Using SMOTE balanced the data and maintained high performance

Decision Tree consistently outperformed Logistic Regression

ROC Curve showed stronger AUC for the tree model

Final model saved using joblib for reuse

License

This project is intended for educational and research purposes as part of the Elevvo Pathways ML Internship.

