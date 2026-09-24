# Expense_Savings_Predictor.ipynb
A financial data analysis machine learning pipeline built using Python technology analyzes over 116,000 bank transactions for expenditure rhythms and predictions of monthly spend as well as savings using Random Forest regression.
# Smart Expense & Savings Predictor

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1xWLCNlYHIdKCtjz-_UaJK7jNu45eM9JJ#scrollTo=CT0qb5pqLzsi)

## 📌 Project Overview
Personal financial management often lacks predictive foresight—traditional budgeting applications show historical spending but fail to project where cash flow is heading.

This project addresses that operational gap by building an end-to-end predictive financial analytics engine in Python. Using a real-world dataset of **116,201 bank transaction records** across multiple accounts from 2015 to 2019, the pipeline cleans raw ledger descriptions, constructs time-dependent features, and trains a **Random Forest Regressor** to forecast next-month expenditures and net savings rates.

---

## 🛠️ Key Features & Methodology
- **Data Cleaning & Preprocessing:** Standardizes dates, balances, deposits, and withdrawal ledgers across 116k+ transaction logs.
- **Rule-Based Categorization:** Implements regular expression pattern matching to group raw transaction descriptions into core operational categories (*Fund Transfers, Cash Withdrawals, Cheque Clearings, POS/Retail, Bank Charges*).
- **Time-Series Feature Engineering:**
  - Constructs month-over-month lag variables (`Expense_Lag1`, `Expense_Lag2`, `Inflow_Lag1`) to capture temporal dependency.
  - Computes 3-month and 6-month rolling window moving averages (`Expense_Rolling3`, `Expense_Rolling6`) to smooth spending trend volatility.
- **Ensemble Machine Learning:** Trains and evaluates a **Random Forest Regressor** using sequential chronological splitting to forecast future monthly outflows (evaluated via MAE, RMSE, and R²).
- **Automated Financial Advisory Engine:** Evaluates projected cash flow against the 50/30/20 budget framework to flag low-liquidity risks and recommend actionable savings targets.

---

## 📊 Dataset Specifications
- **File Name:** `bank.xlsx`
- **Total Records:** 116,201 transaction logs
- **Time Horizon:** 2015 – 2019
- **Core Variables:** `Account No`, `DATE`, `TRANSACTION DETAILS`, `WITHDRAWAL AMT`, `DEPOSIT AMT`, `BALANCE AMT`

---

## 🧰 Tech Stack
- **Language:** Python 3.x
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning & Modeling:** Scikit-Learn (Random Forest Regressor, Regression Metrics)
- **Data Visualization:** Seaborn, Matplotlib
- **Environment:** Google Colab / Jupyter Notebook

---

## 🚀 How to Run
1. Click the **Open In Colab** badge above to launch the notebook directly in your browser.
2. Upload `bank.xlsx` to your Google Colab session storage panel (left sidebar 📁).
3. Execute all code cells sequentially (`Shift + Enter`).
