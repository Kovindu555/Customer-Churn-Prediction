# 📞 Telco Customer Churn Prediction: DT vs. Neural Networks

## Project Overview

This repository contains the complete implementation and analysis for a binary classification task focused on predicting customer churn within a telecommunications dataset. The project compares the performance of a traditional **Decision Tree (DT) model** against a modern **Neural Network (NN) model** to identify the most effective strategy for customer retention.

## Key Features

* **Problem:** Binary classification to predict `Churn` (Yes/No).
* **Data Preparation:** Extensive Exploratory Data Analysis (EDA), cleaning of the `TotalCharges` column, and feature transformation.
* **Imbalance Handling:** Use of the **SMOTE** technique applied only to the training set to mitigate class imbalance bias.
* **Model Comparison:** Implementation and evaluation of four models:
    * DT Baseline
    * DT Tuned (via `GridSearchCV`)
    * NN Baseline (Keras/TensorFlow)
    * NN Tuned (via `KerasTuner` **RandomSearch**)
* **Evaluation:** Focus on business-critical metrics: F1-score (for the minority class) and ROC-AUC.
* **Ethics:** Discussion of AI ethical considerations (bias, fairness, transparency) and post-deployment monitoring strategy.

## Repository Contents

* `EDA.ipynb`: Jupyter notebook detailing initial data exploration and cleaning steps.
* `Trained_Churn_Predictior.ipynb`: Jupyter notebook containing all preprocessing, model building, hyperparameter tuning, and final evaluation code.
* `train_ready_churn_dataset.csv`: The clean, preprocessed dataset ready for model consumption.
* `README.md`: This document.
* `Report.pdf` (Placeholder): The final written report detailing the methodology and results.

## Final Performance Summary

The **Tuned Neural Network** model achieved the highest performance, demonstrating the best balance between Precision and Recall.

| Model | F1-Score (Churn) | ROC-AUC |
| :--- | :--- | :--- |
| DT Baseline | 0.5191 | 0.6715 |
| DT Tuned | 0.6065 | 0.8073 |
| NN Baseline | 0.5824 | 0.8091 |
| **NN Tuned** | **0.6132** | **0.8202** |
