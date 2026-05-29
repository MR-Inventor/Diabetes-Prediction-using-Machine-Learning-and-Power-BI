# Diabetes Prediction using Machine Learning and Power BI

## 📌 Project Overview

This project focuses on predicting diabetes using Machine Learning algorithms and visualizing insights through Power BI dashboards. The system helps in early diabetes detection by analyzing medical attributes and generating accurate predictions for clinical decision support.

---

## 👨‍💻 Research Team

- **Digvijay Patankar**
- **Sushant Deolgaonkar**

---

# 🛠️ Tech Stack

## Machine Learning
- Scikit-learn
- XGBoost

## Data Processing
- Pandas
- NumPy

## Visualization
- Power BI

## Deployment
- Python Pickle

---

# 🎯 Problem Statement

Early detection of diabetes is essential to prevent severe health complications and improve long-term patient outcomes.

The objective of this project is to:
- Develop a predictive model using patient medical data
- Identify diabetes risk before symptoms appear
- Use Machine Learning to uncover hidden patterns in healthcare data

---

# 📊 Dataset Overview

## Dataset Used
### PIMA Indians Diabetes Dataset

A well-known medical dataset containing diagnostic measurements from female patients of Pima Indian heritage aged 21 and above.

### Dataset Information
- **Total Patients:** 768
- **Features:** 9
- **Classes:** 2

---

## Important Features

- Glucose
- BMI
- Insulin
- Blood Pressure
- Age
- Pregnancies

### Target Variable
- `0` → No Diabetes
- `1` → Diabetes

---

# ⚙️ Data Preprocessing Pipeline

## 1. Data Cleaning
- Replaced medically impossible zero values with `NaN`

## 2. Missing Value Handling
- Used `SimpleImputer`
- Median strategy applied to preserve statistical properties

## 3. Feature Scaling
- Applied `StandardScaler`
- Normalized feature ranges for better model training

## 4. Train-Test Split
- Used `80:20` ratio
- Applied stratification to maintain class balance

---

# 🤖 Machine Learning Models Used

## Logistic Regression
Baseline linear model providing interpretable probability estimates.

## Random Forest Classifier
Ensemble-based algorithm capable of handling non-linear relationships while reducing overfitting.

## XGBoost Classifier
Advanced gradient boosting model optimized for performance and accuracy.

---

# 🔍 Validation Strategy

## Stratified K-Fold Cross Validation
- 5-fold splits
- Maintains class distribution
- Reduces variance

## Evaluation Metric
### ROC-AUC Score
Measures the model’s capability to distinguish between diabetic and non-diabetic patients.

---

# ⚡ Hyperparameter Optimization

Used `RandomizedSearchCV` for efficient hyperparameter tuning.

## Parameters Tuned
- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

## Best Performing Model
✅ Tuned Random Forest Classifier

---

# 📈 Model Performance

| Metric | Score |
|--------|--------|
| Accuracy | 82% |
| Precision | 79% |
| Recall | 76% |
| ROC-AUC | 0.87 |

---

# 🚀 Model Deployment

## Features
- Serialized model using `best_model.pkl`
- Flask API integration ready
- Real-time prediction support
- Production monitoring framework included

---

# 📊 Power BI Dashboard Features

## Interactive Analytics
- Feature importance visualization
- Model performance comparison
- Patient risk segmentation
- Interactive filters and reports

The Power BI dashboard converts raw predictions into actionable clinical insights for healthcare professionals.

---

# 📂 Project Structure

```bash
Diabetes-Prediction/
│
├── data/
├── notebooks/
├── models/
│   └── best_model.pkl
├── powerbi/
├── app.py
├── requirements.txt
└── README.md
