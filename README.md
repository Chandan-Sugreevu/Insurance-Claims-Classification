# Insurance Claims Classification (PySpark)

This repository presents a complete pipeline for predicting insurance claim outcomes using **PySpark**, enabling scalable and efficient processing for diverse datasets.

## Table of Contents
- Project Overview
- Features
- Data & Preprocessing
- Modeling & Evaluation
- Getting Started
- Results
- Contact

## Project Overview

Predict whether a customer will file an insurance claim based on demographic and vehicle data. Built with **PySpark**, this project is designed to handle large-scale data processing while maintaining accuracy and performance.

## Features

- Data cleaning, handling missing values and duplicates
- Encoding of categorical variables with PySpark StringIndexer and OneHotEncoder
- Feature extraction using PySpark UDFs (e.g., parsing torque and power values)
- Class balancing using SMOTE for imbalanced data
- Modeling with PySpark MLlib: Random Forest and Support Vector Machine (SVM)
- Hyperparameter tuning with CrossValidator and Randomized Search

## Data & Preprocessing

- **Dataset:** Insurance claims data.csv
- **Target:** Claim Status (0 = No, 1 = Yes)
- **Features:** Includes customer age, vehicle specs, subscription length, region code, fuel type, engine type, etc.
- Steps include:
  - Cleaning missing and duplicate records
  - Encoding categorical variables with StringIndexer and OneHotEncoder
  - Extracting numeric details from text fields with PySpark UDFs
  - Standardizing numeric features with StandardScaler

## Modeling & Evaluation

- **Train-test split:** 80% training, 20% testing
- **Class imbalance:** Addressed using SMOTE
- **Models:**
  - Random Forest Classifier
  - Support Vector Machine (sigmoid kernel)
- **Hyperparameter tuning:** Using PySpark CrossValidator
- **Metrics:** Accuracy, Precision, Recall, F1 Score, Confusion Matrix


## Results

| Model           | Accuracy | Precision | Recall | F1 Score |
|-----------------|----------|-----------|--------|----------|
| Random Forest   |   0.87   |   0.85    |  0.81  |   0.83   |
| SVM (sigmoid)   |   0.79   |   0.77    |  0.73  |   0.75   |

Random Forest performed best after hyperparameter tuning.
