# Heart Disease Prediction Project

This project demonstrates a complete workflow for predicting Heart Disease using machine learning, including data exploration, feature analysis, model training, ensemble learning, and explainability with SHAP.

---

## Table of Contents
- [Dataset Overview](#dataset-overview)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Baseline Models](#baseline-models)
- [Ensemble & Stacked Models](#ensemble--stacked-models)
- [Feature Importance & SHAP Analysis](#feature-importance--shap-analysis)
- [Model Evaluation](#model-evaluation)
- [Submission](#submission)

---

## Dataset Overview

The dataset contains features related to patient demographics, health metrics, and risk factors. The target variable is `Heart Disease` (0 = absence, 1 = presence).  

### Target Distribution
The dataset was analyzed to understand class distribution:

![Target Distribution](Images/target_distribution.png)

---

## Exploratory Data Analysis (EDA)

EDA was performed to examine missing values, feature distributions, and correlations between features. This step ensures the dataset is clean and ready for modeling.

---

## Baseline Models

Several baseline models were trained and evaluated on ROC-AUC and Log Loss:

- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- XGBoost  
- LightGBM  

### Feature Importance (Random Forest)
A Random Forest model was used to estimate the most influential features:

![Random Forest Feature Importance](Images/random_forest_feature_importance.png)

### ROC Curves (Baseline Models)
Performance comparison of baseline models using ROC curves:

![Baseline Model ROC Curves](Images/baseline_model_roc_curves.png)

### Confusion Matrix (XGBoost)
Example confusion matrix for the XGBoost model:

![XGBoost Confusion Matrix](Images/xgboost_confusion_matrix.png)

### Feature Importance (XGBoost)
XGBoost feature importances for interpretability:

![XGBoost Feature Importance](Images/xgboost_feature_importance.png)

---

## Ensemble & Stacked Models

A Stacked Ensemble combines Random Forest, Gradient Boosting, XGBoost, and LightGBM as base models, with Logistic Regression as the meta-learner.  

### ROC Curve (Ensemble vs Base Models)
Comparison between base models and stacked ensemble:

![Ensemble vs Models ROC Curve](Images/ensemble_vs_models_roc_curve.png)

### Confusion Matrix (Stacked Model)
Confusion matrix of the final stacked ensemble model:

![Stacked Model Confusion Matrix](Images/stacked_model_confusion_matrix.png)

---

## Feature Importance & SHAP Analysis

SHAP (SHapley Additive exPlanations) was used to explain predictions from the best-performing model:

### SHAP Summary Plot
Overview of feature contributions:

![SHAP Summary Plot](Images/shap_summary_plot.png)

### SHAP Feature Importance
Feature importance based on SHAP values:

![SHAP Feature Importance](Images/shap_feature_importance.png)

### SHAP Dependence Plot
Illustrates the interaction effect of a key feature:

![SHAP Dependence Plot](Images/shap_dependence_plot.png)

---

## Model Evaluation

The final stacked ensemble model achieved:

- ROC-AUC: 0.9551  
- Log Loss: 0.2786  
- Optimal F1-Score Threshold: 0.392

These metrics indicate strong predictive performance for Heart Disease detection.

---




---

**Author:** Omar Jebbari  
**Date:** 2026-03-05  
