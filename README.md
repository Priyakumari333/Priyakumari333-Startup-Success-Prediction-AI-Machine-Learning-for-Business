# 🚀 Startup Success Prediction Using Machine Learning

## 📌 Overview

Predicting startup success is a complex challenge influenced by multiple financial, operational, and market-related factors. This project applies machine learning techniques to predict whether a startup is likely to be successful or unsuccessful using key business indicators such as funding, valuation, revenue, customer base, age, and industry.

The solution is designed as a data-driven decision-support tool that can assist investors, venture capital firms, and startup founders in evaluating startup potential and reducing investment risk.

---

## 🎯 Business Objective

Many startups fail despite receiving substantial funding. Traditional evaluation methods often rely on intuition and subjective judgment.

This project aims to:

- Predict startup success using historical startup data.
- Support venture capital and investment decisions.
- Enable data-driven risk assessment.
- Identify the factors that contribute most to startup success.
- Provide transparent and interpretable predictions.

---

## 📊 Dataset

**Dataset:** Global Startup Success Dataset

The dataset contains information on **5,000 startups** across multiple industries and countries.

### Features

| Feature | Description |
|----------|------------|
| Founded Year | Year startup was established |
| Industry | Startup industry sector |
| Total Funding ($M) | Total funding received |
| Annual Revenue ($M) | Annual revenue generated |
| Valuation ($B) | Company valuation |
| Customer Base (Millions) | Number of customers |
| Number of Employees | Employee count |
| Social Media Followers | Online audience size |
| Funding Stage | Startup maturity stage |
| Country | Startup headquarters location |

---

## 🔍 Exploratory Data Analysis

Key findings from EDA:

- No missing values were present in the dataset.
- Numerical variables exhibited extremely weak correlations.
- Success Score showed little predictive value and was removed.
- Industry-specific differences were identified across funding, revenue, valuation, and customer base.
- Industry normalization was required to ensure fair comparisons between startups.

### Major Insights

✅ Balanced representation across industries and countries.

✅ No significant outliers detected.

✅ Financial metrics were the strongest indicators of startup success.

✅ Industry-level normalization improved fairness and model reliability.

---

## ⚙️ Data Preparation

### Feature Engineering

A new binary target variable called **Success_Flag** was created.

To ensure fairness across industries:

1. Valuation
2. Revenue
3. Funding
4. Customer Base
5. Startup Age

were normalized within their respective industries.

A weighted performance score was then calculated:

| Feature | Weight |
|----------|---------|
| Valuation | 25% |
| Funding | 25% |
| Revenue | 20% |
| Customer Base | 20% |
| Age | 10% |

Startups above the 75th percentile within their industry were classified as:

- **1 = Successful**
- **0 = Unsuccessful**

### Preprocessing Steps

- Removed low-value features
- One-Hot Encoding
- Standard Scaling
- Stratified Train-Test Split (80/20)

---

## 🤖 Machine Learning Models

The following classification algorithms were implemented:

### 1. Logistic Regression
- Baseline model
- High interpretability
- Strong generalization

### 2. Decision Tree
- Captures nonlinear relationships
- Easy visualization

### 3. K-Nearest Neighbors (KNN)
- Distance-based classification
- Tuned using cross-validation

### 4. Naive Bayes
- Probabilistic classifier
- Fast and lightweight

### 5. Random Forest
- Ensemble learning
- Feature importance analysis

### 6. XGBoost
- Gradient boosting framework
- Excellent performance on tabular data

---

## 📈 Model Performance

| Model | Accuracy | ROC-AUC |
|---------|---------|---------|
| Logistic Regression | 96.9% | 0.997 |
| Decision Tree | 91.6% | 0.882 |
| KNN | 94.2% | 0.985 |
| Naive Bayes | 90.8% | 0.990 |
| Random Forest | 95.5% | 0.993 |
| XGBoost | 97.1% | 0.995 |

---

## 🏆 Final Model

### Logistic Regression

Although XGBoost achieved slightly higher accuracy, Logistic Regression was selected as the final model because it provided:

- Better balance between precision and recall
- Fewer missed successful startups
- Strong cross-validation performance
- Higher interpretability for business stakeholders

### Final Metrics

| Metric | Value |
|----------|---------|
| Accuracy | 96.9% |
| ROC-AUC | 0.997 |
| Cross-Validation Accuracy | 97.3% |
| False Positives | 27 |
| False Negatives | 4 |

---

## 📌 Key Business Insights

The most influential factors driving startup success were:

1. Total Funding
2. Valuation
3. Annual Revenue
4. Customer Base
5. Startup Age

These findings suggest that financial strength and market traction are the strongest predictors of startup success.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📂 Project Structure

```text
Startup-Success-Prediction/
│
├── data/
│   └── global_startup_success_dataset.csv
│
├── notebooks/
│   ├── EDA.ipynb
│   ├── Data_Preprocessing.ipynb
│   └── Model_Training.ipynb
│
├── models/
│   └── logistic_regression_model.pkl
│
├── reports/
│   └── Project_Report.pdf
│
├── requirements.txt
│
└── README.md
```

---

## 💼 Business Impact

This project demonstrates how machine learning can support investment and startup evaluation decisions by transforming raw startup data into actionable insights.

Potential applications include:

- Venture Capital Screening
- Startup Risk Assessment
- Investment Portfolio Analysis
- Startup Benchmarking
- Strategic Business Planning

---

## 👥 Contributors

- Priya Kumari
- Chris Caitan Ruzario
- Asif Ahmed

---

## 📜 Academic Context

This project was completed as part of:

**CS6471- Artificial Intelligence & Machine Learning for Business**

**MSc Business Analytics**

**University of Limerick**

---

## ⭐ If you found this project useful, consider giving it a star!
