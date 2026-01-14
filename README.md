# 📊 Credit Risk Prediction Project

## 📌 Project Overview
This project builds a **machine learning classification system** to predict whether a **loan applicant is likely to default** based on financial and demographic information.

The goal is to **support credit risk assessment** by identifying high-risk applicants **before loan approval**, which is a real-world problem faced by banks and financial institutions.

---

## 🎯 Objective
Predict whether a loan applicant will **default (Yes)** or **not default (No)** using historical loan data.

This directly fulfills the objective:
> **“Predict whether a loan applicant is likely to default on a loan.”**

---

## 📂 Dataset
- **Source:** Loan Prediction Dataset (Kaggle)
- **Target Variable:** `Loan_Status`
  - `Y` → Loan approved / No default  
  - `N` → Loan rejected / Default risk

### Key Features Used:
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Education
- Gender
- Property Area
- Self Employment Status

---

## 🛠️ Project Workflow

### 1️⃣ Data Cleaning & Preprocessing
- Handled missing values using:
  - **Median** for numerical features
  - **Mode** for categorical features
- Converted categorical variables into numeric format
- Checked class balance

---

### 2️⃣ Exploratory Data Analysis (EDA)
- Visualized:
  - Loan Amount distribution
  - Income vs Loan Status
  - Education vs Loan Approval
- Identified **Credit History** as the strongest predictor

---

### 3️⃣ Model Training
Two classification models were trained:

| Model | Reason |
|------|--------|
| Logistic Regression | Baseline, interpretable |
| Decision Tree Classifier | Captures non-linear patterns |

---

### 4️⃣ Model Evaluation
Each model was evaluated using:
- Accuracy
- Confusion Matrix (visualized)
- ROC-AUC Score
- Feature Importance (Decision Tree)

---

## 📈 Model Performance Summary

### 🔹 Logistic Regression
- High interpretability
- Performs well on linear relationships
- ROC-AUC indicates reasonable discrimination ability

⚠️ Required **feature scaling** and higher `max_iter` to converge properly

---

### 🔹 Decision Tree
- Captures complex, non-linear relationships
- Easier to visualize decision logic
- Risk of overfitting if not controlled

---

### 🔄 ROC-AUC Comparison

| Model | ROC-AUC |
|------|--------|
| Logistic Regression | Moderate |
| Decision Tree | Comparable / Slightly higher |

➡️ Decision Tree showed **slightly better separation** between defaulters and non-defaulters.

---

## 📊 Confusion Matrix Interpretation
For both models:

- **True Negatives:** Correctly predicted non-defaulters
- **False Positives:** Rejected good applicants
- **False Negatives:** Approved defaulters (**highest risk**)
- **True Positives:** Correctly predicted defaulters

> Minimizing **False Negatives** is critical in credit risk problems.

---

## 🔍 Key Insights

- **Credit History** is the most influential feature
- Applicants with:
  - Low income
  - High loan amounts
  - Poor credit history  
  are significantly more likely to default
- Decision Tree provides clearer rule-based explanations
- Logistic Regression is safer for regulated environments due to transparency

---

## ✅ Conclusion
This project successfully builds and evaluates machine learning models that:
- Predict loan default risk
- Provide explainable insights
- Reflect real-world banking decision logic

It **fully satisfies the project objective** and is suitable for:
- Data science portfolios
- Entry-level ML roles
- Academic submissions

---

## 🚀 Future Improvements
- Feature scaling for Logistic Regression
- Hyperparameter tuning
- Cross-validation
- Cost-sensitive learning to penalize false negatives
- Ensemble models (Random Forest, XGBoost)

---

## 🧠 Skills Demonstrated
- Data preprocessing
- Exploratory Data Analysis
- Classification modeling
- Model evaluation & interpretation
- Financial risk analytics

---

## 📎 Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
