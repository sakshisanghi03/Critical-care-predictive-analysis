# Critical-care-predictive-analysis

## Overview

This project focuses on predicting critical patient outcomes in Intensive Care Units (ICUs) using Machine Learning techniques. The study analyzes patient physiological measurements and clinical indicators to develop predictive models for:

- ICU Mortality Prediction
- Length of Stay (LOS) Prediction
- Outcome Risk Stratification
- Clinical Decision Support

The objective is to assist healthcare providers in identifying high-risk patients early and improving resource allocation within critical care environments.

---

## Project Objectives

### Mortality Prediction
Develop classification models capable of predicting whether a patient is at risk of mortality during ICU admission.

### Length of Stay Prediction
Develop predictive models to estimate ICU length of stay using patient physiological and clinical features.

### Model Refinement
Improve baseline model performance through:

- Feature Engineering
- Hyperparameter Optimization
- Class Imbalance Handling
- Model Evaluation and Comparison

---

## Dataset

The dataset contains anonymized ICU patient records including:

- Demographic Information
- Physiological Measurements
- Vital Sign Indicators
- Clinical Assessment Variables
- Outcome Variables

Target Variables:

1. Mortality (Binary Classification)
2. Length of Stay (Regression)

---

## Repository Structure

```text
Critical-care-predictive-analysis/
│
├── input.csv
│
├── eda.ipynb
├── eda2.ipynb
│
├── mortality_modeling.ipynb
├── los_modeling.ipynb
│
├── summer_mortality_baseline_refinement.ipynb
├── summer_los_baseline_refinement.ipynb
│
├── file1.ipynb
├── file2.ipynb
├── file3.ipynb
│
├── stats_output/
│   ├── descriptive_statistics
│   ├── feature_analysis
│   └── visualizations
│
├── model_output/
│   ├── trained_models
│   ├── evaluation_results
│   └── performance_metrics
│
└── README.md
```

---

## Methodology

### 1. Exploratory Data Analysis (EDA)

Performed comprehensive data exploration including:

- Missing Value Analysis
- Feature Distributions
- Correlation Analysis
- Class Distribution Assessment
- Outcome Analysis
- Temporal Trend Exploration

### 2. Data Preprocessing

- Missing Value Handling
- Feature Scaling
- Encoding of Variables
- Outlier Detection
- Data Cleaning

### 3. Feature Engineering

Created additional predictive variables through:

- Statistical Aggregations
- Physiological Risk Indicators
- Clinical Feature Transformations

### 4. Model Development

#### Mortality Prediction

Machine Learning Models:

- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

#### Length of Stay Prediction

Regression Models:

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

Evaluation Metrics:

- MAE
- RMSE
- R² Score

---

# Results

## ICU Mortality Prediction

The mortality prediction study evaluated multiple machine learning models using baseline training, hyperparameter tuning, SMOTE oversampling, and threshold optimization.

### Best Mortality Model

**Random Forest + SMOTE + Threshold = 0.35**

| Metric | Value |
|----------|----------|
| Accuracy | 95.74% |
| Recall | 35.35% |
| Precision | 23.03% |
| F1 Score | 27.89% |
| ROC-AUC | 0.8708 |
| PR-AUC | 0.1565 |
| Balanced Accuracy | 0.6627 |
| MCC | 0.2642 |

### Key Findings

- Random Forest consistently outperformed Logistic Regression.
- SMOTE improved minority-class detection.
- Threshold optimization significantly improved recall and F1-score.
- The final Random Forest model achieved the highest overall ranking.

---

## ICU Length of Stay (LOS) Prediction

Several machine learning models were evaluated for predicting patient length of stay.

### Best LOS Model

**Random Forest (Tuned + Threshold = 0.35)**

| Metric | Value |
|----------|----------|
| Accuracy | 70.62% |
| Recall | 87.70% |
| Precision | 65.37% |
| F1 Score | 74.90% |
| ROC-AUC | 0.8129 |
| PR-AUC | 0.8149 |
| Balanced Accuracy | 70.63% |
| MCC | 0.4389 |

### Key Findings

- Random Forest achieved the strongest overall performance.
- Hyperparameter tuning improved model stability.
- Threshold optimization improved sensitivity while maintaining acceptable precision.
- Logistic Regression provided a strong baseline but was consistently outperformed by Random Forest.

---

## Model Comparison Summary

| Task | Best Model | Key Metric |
|--------|------------|------------|
| Mortality Prediction | Random Forest + SMOTE + Threshold 0.35 | ROC-AUC = 0.8708 |
| LOS Prediction | Random Forest + Tuned + Threshold 0.35 | F1 = 0.749 |

---
## Project Highlights

✔ Predicted ICU Mortality Risk using Machine Learning

✔ Predicted ICU Length of Stay (LOS)

✔ Applied SMOTE for class imbalance handling

✔ Performed Hyperparameter Optimization

✔ Achieved ROC-AUC of 0.8708 for Mortality Prediction

✔ Achieved F1 Score of 0.749 for LOS Prediction

✔ Extended baseline models through Summer Semester refinement work

---

## Future Work

- Temporal Modeling using LSTM/GRU networks
- Explainable AI (SHAP/LIME)
- ICU Risk Stratification Dashboard
- Real-time Clinical Decision Support
- Multi-horizon Patient Outcome Forecasting

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- SciPy

### Development Environment

- Jupyter Notebook

---

## Results

The developed machine learning models successfully identify patterns associated with:

- ICU Mortality Risk
- Patient Length of Stay
- Clinical Outcome Prediction

Model performance demonstrates the feasibility of applying machine learning techniques to support critical care decision-making.

---

## Author

**Sakshi Sanghi**

Master of Science – Data Science

Wright State University

---

## Disclaimer

This project is intended solely for academic and research purposes. Predictions generated by these models should not be used as a substitute for professional medical judgment or clinical decision-making.
