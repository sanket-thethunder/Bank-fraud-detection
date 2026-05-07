<div align="center">

# 🏦 Bank Fraud Detection

### An end-to-end Machine Learning pipeline to detect fraudulent bank transactions with high precision

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> _"Every fraudulent transaction avoided is a customer's trust preserved."_

<br/>

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Methodology](#-methodology)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Results](#-results)
- [Contributing](#-contributing)

---

## 🔍 Overview

Financial fraud is a billion-dollar problem that affects banks, merchants, and customers globally. This project builds a **supervised machine learning model** that can automatically identify potentially fraudulent bank transactions based on historical labeled data.

The pipeline covers everything from raw data ingestion and exploratory analysis to model training, evaluation, and performance tuning — all within an interactive Jupyter Notebook.

---

## 🚨 Problem Statement

> Given a set of anonymized bank transactions, **classify each transaction as fraudulent or legitimate**.

Fraud detection is inherently a **class imbalance problem** — fraudulent transactions make up a tiny fraction of all activity. This project addresses that challenge head-on using appropriate resampling strategies, evaluation metrics, and model selection.

---

## 📂 Dataset

The project uses two CSV files:

| File | Description |
|------|-------------|
| `transactions_obf.csv` | Anonymized transaction records with features such as amount, merchant type, time, etc. |
| `labels_obf.csv` | Ground-truth labels indicating whether each transaction is fraudulent (`1`) or not (`0`) |

> **Note:** Data has been obfuscated to protect privacy while retaining the statistical structure required for model training.

---

## 🗂 Project Structure

```
Bank-fraud-detection/
│
├── 📓 Fraud_detection_in_bank_update.ipynb   # Main notebook: EDA → Preprocessing → Modeling
├── 📊 transactions_obf.csv                   # Feature data for all transactions
├── 🏷️  labels_obf.csv                         # Fraud labels (target variable)
└── 📄 README.md                              # You are here
```

---

## 🧪 Methodology

The notebook follows a structured ML workflow:

```
Raw Data
   │
   ▼
📊 Exploratory Data Analysis (EDA)
   │  • Class distribution analysis
   │  • Feature correlation heatmaps
   │  • Transaction amount distributions
   │
   ▼
🔧 Data Preprocessing
   │  • Merging transactions with labels
   │  • Handling missing values
   │  • Feature engineering & scaling
   │  • Train/test split
   │
   ▼
⚖️  Handling Class Imbalance
   │  • SMOTE / undersampling strategies
   │  • Weighted loss functions
   │
   ▼
🤖 Model Training
   │  • Logistic Regression (baseline)
   │  • Random Forest Classifier
   │  • Gradient Boosting (XGBoost / LightGBM)
   │
   ▼
📈 Evaluation
      • Confusion Matrix
      • Precision, Recall, F1-Score
      • ROC-AUC Curve
      • PR-AUC (key metric for imbalanced data)
```

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.8+** | Core programming language |
| **Jupyter Notebook** | Interactive development environment |
| **Pandas & NumPy** | Data manipulation and numerical computing |
| **Matplotlib & Seaborn** | Data visualization |
| **Scikit-learn** | ML models, preprocessing, and evaluation |
| **imbalanced-learn** | SMOTE and resampling techniques |
| **XGBoost / LightGBM** | Gradient boosted tree models |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3.8+ and pip installed.

### 1. Clone the repository

```bash
git clone https://github.com/sanket-thethunder/Bank-fraud-detection.git
cd Bank-fraud-detection
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost lightgbm jupyter
```

### 3. Launch the notebook

```bash
jupyter notebook Fraud_detection_in_bank_update.ipynb
```

### 4. Run all cells

Use **Kernel → Restart & Run All** to execute the full pipeline from data loading to model evaluation.

---

## 📊 Results

The model is evaluated using metrics that are meaningful for **imbalanced classification**:

| Metric | Why It Matters |
|--------|---------------|
| **Precision** | Of all flagged fraud cases, how many were actually fraud? |
| **Recall** | Of all real fraud cases, how many did we catch? |
| **F1-Score** | Harmonic balance between Precision and Recall |
| **ROC-AUC** | Overall discriminative ability of the model |
| **PR-AUC** | Performance under extreme class imbalance |

> Accuracy alone is **misleading** for fraud detection — a model predicting "no fraud" every time can achieve 99%+ accuracy yet be completely useless.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get involved:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/improve-model`
3. **Commit** your changes: `git commit -m "Add feature: XGBoost tuning"`
4. **Push** to the branch: `git push origin feature/improve-model`
5. **Open** a Pull Request

Please ensure your code is well-commented and follows the existing notebook structure.

---

## 📬 Author

**Sanket** — [@sanket-thethunder](https://github.com/sanket-thethunder)

---

<div align="center">

⭐ **If you found this project helpful, please give it a star!** ⭐

Made with ❤️ and a lot of ☕

</div>
