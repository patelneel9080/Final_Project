![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Version](https://img.shields.io/badge/version-1.0.0-orange)
![Language](https://img.shields.io/badge/language-Python-blue)

---

# 📊 Holistic Data Preparer (End-to-End ML Data Pipeline)

## 📖 Overview

This project demonstrates a complete **end-to-end data preprocessing and feature engineering pipeline** for a **Customer Credit Risk dataset**.

It simulates a real-world fintech scenario where data is collected from **multiple sources (CSV, JSON, SQL, API)** and transformed into a **machine learning-ready dataset**.

The pipeline covers everything from:

* Data acquisition
* Data cleaning
* Missing value handling
* Outlier detection
* Encoding & scaling
* Feature engineering
* Final dataset generation

---

## 🎯 Objective

To build a **robust and scalable preprocessing pipeline** that prepares raw financial data for predicting:

> ⚡ **Loan Default (0 = No, 1 = Yes)**

---

## 🧠 Problem Statement

You are working as a **Junior Data Scientist** in a fintech company.

Your task is to:

* Clean and preprocess customer data
* Handle missing values and outliers
* Perform feature engineering
* Integrate external API data
* Deliver a **final ML-ready dataset**

---

## 🗂️ Dataset Description

The dataset includes:

### 👤 Demographics

* age
* gender
* region
* education_level
* employment_type

### 💰 Financial Data

* annual_income
* loan_amount
* loan_purpose
* credit_score

### 📈 Behavioral Data

* repayment_history
* transaction_count
* spending_ratio

### 🎯 Target

* default_flag (0 / 1)

---

## 🌐 Data Sources

| Source | Description                  |
| ------ | ---------------------------- |
| CSV    | Main dataset                 |
| JSON   | Metadata/schema              |
| SQL    | Transaction-level records    |
| API    | External economic indicators |

---

## ⚙️ Project Workflow

### 🔹 1. Data Acquisition

* Load CSV using Pandas
* Read JSON metadata
* Fetch SQL data
* Call real-world API (World Bank / Exchange Rate)

---

### 🔹 2. Data Understanding

* `.info()`, `.describe()`
* Missing value analysis
* Data profiling

---

### 🔹 3. Data Cleaning

#### Missing Value Handling

* Simple Imputer (Mean / Mode)
* Most Frequent Imputation
* Missing Indicator
* Random Sampling
* KNN Imputer
* MICE Algorithm

---

### 🔹 4. Outlier Handling

* Z-score method
* IQR method
* Percentile method
* Winsorization

---

### 🔹 5. Feature Engineering

#### Encoding

* Ordinal Encoding → education_level
* Label Encoding → gender
* One-Hot Encoding → region, loan_purpose

#### Date Features

* Extract Year, Month, Weekday from join_date

#### Binning

* Quantile binning
* K-Means binning

---

### 🔹 6. Feature Scaling

* Standardization (Z-score)
* Min-Max Scaling
* MaxAbs Scaling
* Robust Scaling

---

### 🔹 7. Feature Construction

* Debt-to-Income Ratio
* Average Monthly Transactions
* Spending-to-Income Ratio

---

### 🔹 8. Transformations

* Log transformation
* Square root transformation
* Box-Cox / Yeo-Johnson

---

### 🔹 9. Pipeline Implementation

* ColumnTransformer
* Scikit-learn Pipelines

---

## 📊 API Integration

Real-world external data is fetched using:

* 🌐 World Bank API (GDP, Inflation, Interest Rate)
* 💱 Exchange Rate API

Example:

```python
import requests

response = requests.get("https://api.worldbank.org/v2/country/IND/indicator/NY.GDP.MKTP.KD.ZG?format=json")
data = response.json()
```

---

## 🧪 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* SQLite
* Requests (API handling)

---

## 🚀 How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Run dataset generation
python src/data_generation.py

# Run preprocessing
python src/preprocessing.py
```

---

## 📈 Final Output

* ✅ Cleaned dataset
* ✅ Feature-engineered dataset
* ✅ ML-ready data
* ✅ Multi-source integrated pipeline

---

## 📌 Key Learnings

* End-to-end data preprocessing workflow
* Handling real-world messy data
* Feature engineering strategies
* API data integration
* Building production-like pipelines

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgment

This project is designed as a **complete hands-on practice for Data Science & Machine Learning preparation**.
