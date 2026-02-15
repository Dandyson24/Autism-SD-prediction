#### Autism Spectrum Disorder (ASD) Prediction Model

**Machine Learning–Based Screening Support for Early ASD Identification**

#### Project Overview

This project presents an end-to-end machine learning pipeline for predicting Autism Spectrum Disorder (ASD) using structured behavioral screening data.

The goal is to develop a screening support model that improves early identification by:

Addressing class imbalance

Preventing data leakage

Reducing overfitting

Optimizing classification thresholds

Ensuring interpretability in a healthcare context

**NB This model is not a diagnostic tool. It is designed to support screening and risk stratification.**

### Background

Autism Spectrum Disorder (ASD) is a neurodevelopmental condition affecting social interaction, communication, and behavior.

Early identification significantly improves intervention outcomes. However, screening tools often produce borderline results. Machine learning can assist by identifying complex patterns across behavioral indicators.

📊 Dataset Description

Structured screening dataset

Behavioral scores (A1–A10)

Age and demographic variables

Binary target variable: Class/ASD

Class imbalance observed (minority ASD cases)

### Exploratory Data Analysis (EDA)
Class Distribution

The dataset showed imbalance between ASD and non-ASD cases.

**Figure 1: Class Distribution Before SMOTE**

![Class Distribution before SMOTE](https://github.com/Dandyson24/Autism-SD-prediction/blob/main/Class%20distribution%20before%20SMOTE.png?raw=true)

Feature Correlation Heatmap

Behavioral scores show moderate inter-feature correlation.

**Figure 2: Correlation Heatmap**

![Correlation Heatmap](https://github.com/Dandyson24/Autism-SD-prediction/blob/main/Confusion_matrix_.png)

⚙️ Methodology
### Data Preprocessing

Data cleaning

Encoding categorical variables

Train-test split (before SMOTE)

Feature scaling (if applicable)

#### Handling Class Imbalance

Applied SMOTE only on training data to prevent data leakage.

**Figure 3: Class Distribution After SMOTE**

![SMOTE Distribution]((https://github.com/Dandyson24/Autism-SD-prediction/blob/main/Class%20distribution%20after%20SMOTE.png)))

####  Model Development

Models tested:

Random Forest Classifier (Primary model)

Regularized version to prevent overfitting

Techniques used:

Cross-validation

Hyperparameter tuning

Depth regularization

Minimum samples constraint

### Model Performance
Initial Model Performance

Training Accuracy: 99%

Test Accuracy: 84%

Evidence of overfitting

Regularized Model Performance

Test Accuracy: ~80%

ROC-AUC: 0.90

Improved generalization

Confusion Matrix

**Figure 4: Confusion Matrix (Test Set)**

![Confusion Matrix](figures/confusion_matrix.png)

#### ROC Curve

**Figure 5: ROC Curve (Test Set)**

![ROC Curve](figures/roc_curve.png)

## Threshold Optimization

Instead of using the default 0.5 probability cutoff:

ROC curve analyzed

Youden’s Index used to determine optimal threshold

Improved sensitivity-specificity balance

 **Figure 6: Threshold Optimization Plot**

![Threshold Optimization](figures/threshold_optimization.png)

####  Feature Importance

The most influential features:

A9_Score

A4_Score

Age

A6_Score

 **Figure 7: Feature Importance Plot**

![Feature Importance](figures/feature_importance.png)

#### Key Metrics (Final Model)
Metric	Value
Accuracy	~80%
ROC-AUC	0.90
Sensitivity	Optimized
Specificity	Balanced
### Technical Skills Demonstrated

Pandas & NumPy

- Exploratory Data Analysis

- SMOTE (Imbalanced Learning)

- Random Forest Modeling

- Cross-Validation

- Hyperparameter Tuning

- Overfitting Diagnosis

- ROC & Threshold Optimization

- Feature Importance Analysis

- Ethical AI in Healthcare

### Ethical Considerations

Not intended for diagnosis

Requires external validation

Risk of bias in screening instruments

Emphasis on sensitivity in early detection

Clinical oversight required

### Future Improvements

SHAP explainability

Calibration curve analysis

Comparison with Logistic Regression & XGBoost

External dataset validation

Streamlit deployment demo

API-based risk scoring simulation

📁 Project Structure
├── data/
├── notebooks/
│   └── Autism_Spectrum_Disorder_Predicting_Model.ipynb
├── figures/
│   ├── class_distribution.png
│   ├── correlation_heatmap.png
│   ├── smote_distribution.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── threshold_optimization.png
│   └── feature_importance.png


👨🏽‍⚕️ Author

Andrew Nwachimere-eze Okebugwu 
Public Health Physician | PhD | Health Data Scientist

GitHub: [Insert Link]

LinkedIn: [Insert Link]

Portfolio: [Insert Link]
