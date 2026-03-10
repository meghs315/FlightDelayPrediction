# Modeling and Predicting Flight Departure Delays

## Overview
This project uses supervised machine learning to predict **flight departure delays** using historical airline data. Delays are influenced by many factors such as airline operations, airport congestion, and time of day. By analyzing historical flight data, we aim to identify patterns that help predict when delays will occur.

## Dataset
We use the **Airlines Delay Analysis** dataset from Kaggle:

https://www.kaggle.com/datasets/sherrytp/airline-delay-analysis/data

The dataset includes information such as:
- Airline
- Origin and destination airports
- Date
- Scheduled departure time (CRS_DEP_TIME)
- Actual departure time
- Departure delay
- Taxi-out and wheels-up times

Some limitations include the absence of external factors like weather and the removal of rows with missing delay values.

## Problem Type
This project explores three supervised learning approaches:

### Binary Classification
Predict whether a flight is **delayed (>15 minutes)** or **not delayed**.

Models:
- Logistic Regression
- Random Forest

### Regression
Predict the **exact delay time in minutes**.

Models:
- Linear Regression
- Tree-based regression models

### Multiclass Classification
Predict the **severity of delay**:
- 0–15 minutes
- 16–30 minutes
- 31–60 minutes
- 60+ minutes

Models:
- Multinomial Logistic Regression
- Random Forest
- Neural Network

## Evaluation
Models are evaluated using an **80/20 train-test split** and **5-fold cross-validation**.

Metrics include:
- **Binary Classification:** F1-score, accuracy, ROC-AUC
- **Regression:** RMSE, MAE, R²
- **Multiclass Classification:** Macro F1-score, accuracy
