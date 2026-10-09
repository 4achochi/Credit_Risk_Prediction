# CREDIT RISK PREDICTION

## Project Overview

This project develops and evaluates machine learning models to predict whether a credit-card client will default on their next payment. It explores how predictive analytics can support credit-risk assessment and data-informed decision-making.

## Objectives

. Explore and understand the credit-card default dataset.
. Investigate patterns associated with payment default.
. Train and compare Logistic Regression, Decision Tree, and Random Forest classifiers.
. Evaluate model performance using accuracy, precision, recall, F1-score, and ROC-AUC.
. Examine classification thresholds under hypothetical business-cost assumptions.
. Interpret model predictions using SHAP.

## Dataset

Our project uses the UCI Default of Credit Card Clients dataset, containing 30,000 client records. The target variable is `default payment next month`.

The dataset has an imbalanced target: approximately 22.12% of observations represent defaults and 77.88% represent non-defaults.

## Methods

1. Data inspection and exploratory analysis
2.Stratified train-test split
3.Logistic Regression with feature scaling
4. Decision Tree classification
5.Random Forest classification
6.Stratified five-fold cross-validation
7.Threshold-based cost comparison
8.SHAP model explainability

## Preliminary Results

On the held-out test set, the Random Forest model achieved:

. Accuracy: 78.3%
. Precision for default: 50.8%
. Recall for default: 58.6%
. F1-score for default: 54.4%
. ROC-AUC: 0.776

These are preliminary results from the current modeling workflow. Final conclusions depend on further validation and review.

## Business Analysis

A hypothetical error-cost analysis compared classification thresholds using assumed costs of KSh 20,000 per missed default and KSh 2,000 per false positive. These values are illustrative, not actual bank loss estimates.

## Explainability

SHAP analysis ranked `PAY_0`, `PAY_2`, and `LIMIT_BAL` among the most influential features in the sample analyzed. Feature importance indicates model behavior, not causation.

## Limitations

- Results depend on the dataset and modeling choices.
- Hypothetical error costs do not capture all real-world credit losses.
- Model performance does not establish suitability for actual lending decisions.
- Fairness, privacy, calibration, and external validation require further assessment.

## Tools

Python, pandas, scikit-learn, Matplotlib, and SHAP.

## Reproducibility

See `requirements.txt` for the Python dependencies. The analysis notebook documents the workflow.

## Disclaimer

This is an educational portfolio project. It is not a production credit-scoring system and should not be used to make actual lending decisions.
