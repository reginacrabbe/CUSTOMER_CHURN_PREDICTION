# Customer Churn Prediction Project

## Overview

This project aims to predict customer churn for a telecom company. Churn prediction helps businesses proactively identify customers who are likely to leave and take necessary retention measures. The project leverages machine learning techniques to develop a predictive model for customer churn based on customer demographic and service usage data.

## Table of Contents

- [Introduction](#introduction)
- [Problem Definition](#problem-definition)
- [Data](#data)
- [Project Steps](#project-steps)
- [Model Evaluation](#model-evaluation)
- [Conclusion](#conclusion)
- [Recommendations](#recommendations)

## Introduction

Customer churn is a critical issue for subscription-based businesses like telecom companies. Identifying which customers are likely to churn can help the company focus on customer retention strategies. By building a predictive model, the company can anticipate customer behavior and implement personalized interventions.

## Problem Definition

The main goal of this project is to build a predictive model that can anticipate customer churn. This can help the telecom company take action to retain high-risk customers by identifying patterns in demographics and service usage.

## Data

The dataset used in this project contains information about telecom customers, including their demographics, account details, and usage patterns. The target variable is `Churn`, indicating whether a customer has churned (1) or not (0).

Key features include:

- Customer tenure
- Monthly charges
- Total charges
- Contract type (monthly, yearly)
- Services subscribed to (internet, phone, etc.)
- Payment method

## Project Steps

1. **Exploratory Data Analysis (EDA)**:
    - Conducted EDA to explore relationships between features and the target variable (`Churn`).
    - Visualized key patterns and performed univariate, bivariate, and multivariate analysis.

2. **Feature Engineering**:
    - Categorical variables were encoded using one-hot encoding.
    - Missing values were handled, and unnecessary columns like `customerID` were dropped.
    - Created new features based on insights from the EDA.

3. **Model Selection and Training**:
    - Trained and evaluated several machine learning models including:
        - Logistic Regression
        - Random Forest
        - Gradient Boosting
        - Support Vector Machine (SVM)
        - K-Nearest Neighbors (KNN)
        - Decision Tree
    - The best model was selected based on performance metrics like accuracy, precision, recall, and F1-score.

4. **Handling Class Imbalance**:
    - Class imbalance was tackled using two methods:
        - **Class Weight Balancing**: Adjusted the class weights in the models to account for the imbalance in the target variable.
        - **SMOTE (Synthetic Minority Over-sampling Technique)**: Used SMOTE to balance the class distribution by oversampling the minority class.

5. **Model Evaluation**:
    - Evaluated models using confusion matrices and classification reports.
    - Analyzed metrics such as accuracy, recall, precision, and F1-score.
    - **Best Model**: After evaluating the models, **Logistic Regression with Class Weight Balancing** was selected for its good balance of precision and recall.

6. **Hyperparameter Tuning**:
    - Performed hyperparameter tuning using GridSearchCV to optimize the Logistic Regression model.
    - The best model achieved a recall score of **0.8021** for predicting churn.

## Model Evaluation

- **Logistic Regression** with class weight balancing emerged as the best model.
- Recall was emphasized because predicting customer churn (class 1) is crucial for the business.
- The final model's recall for class 1 (churn) was 82%, meaning it effectively identifies customers likely to churn, providing actionable insights for retention efforts.

## Conclusion

This project successfully developed a customer churn prediction model. The **Logistic Regression** with class weight balancing proved to be the most effective, achieving a recall score of 0.8021 for predicting churn. This model allows the business to accurately predict which customers are likely to churn, helping them take proactive steps for customer retention.

## Recommendations

1. **Retention Strategy**: Implement targeted retention strategies for customers predicted to churn by offering personalized incentives, discounts, or improved service plans.
2. **Focus on Recall**: Prioritize improving recall to ensure that most churn cases are detected, even at the cost of slightly higher false positives. This approach is crucial for reducing customer attrition.
3. **Feature Enrichment**: Explore additional data sources (e.g., customer service interactions, web behavior) to enrich the model with more predictive features.
4. **Continuous Model Monitoring**: Monitor model performance regularly and retrain with fresh data to maintain accuracy as customer behavior evolves.
