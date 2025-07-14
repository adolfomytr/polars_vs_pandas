# 🐼🔁 Comparing pandas vs Polars (Eager & Lazy Execution) for Banking Data Analysis

## 📌 Introduction

This project presents a **step-by-step performance comparison** between three data processing approaches using the same dataset and analysis logic:

- **pandas**
- **Polars (Eager Execution)**
- **Polars (Lazy Execution)**

The goal is to understand how each library performs in terms of **execution time** and **memory usage**, using a real-world dataset representative of banking and financial transaction data.

This comparison is intended to be educational for **beginner to intermediate Python users**, especially those working in **consulting and financial analytics**.

---

## 🧾 Dataset Description

The dataset used in this project is publicly available on [Kaggle](https://www.kaggle.com/datasets/ismetsemedov/transactions) and simulates transactional activity in a banking environment. It contains:

- **Rows:** 7,000,000+
- **Columns:** 24
- **File Size:** 2.93 GB (CSV)

Each row represents a single customer transaction, and the columns provide details such as transaction date, amount, merchant type, and fraud status.

**Main columns include:**
- `transaction_id`: Transaction ID (unique)
- `timestamp`: Timestamp of the transaction
- `amount`: Transaction amount in local currency
- `customer_id`: Unique customer identifier
- `merchant`: Unique merchant identifier
- `merchant_type`: Category or type of merchant
- `is_fraud`: Binary flag indicating whether the transaction was fraudulent

---

## 🛠️ Project Steps

Each notebook in this repo performs the **same analysis pipeline** using one of the three approaches. The steps are:

1. **Loading the data** from CSV
2. **Exploratory Data Analysis (EDA)**:
   - Transaction count and volume by merchant type
   - Descriptive statistics by transaction type
3. **Feature Engineering & Aggregation**:
   - Monthly transaction totals
   - Unique merchant and customer counts
4. **Fraud Detection Insights**:
   - Fraud ratio by transaction description
   - Fraud frequency by customer
5. **Benchmarking**:
   - Execution time and memory usage per operation
   - Results stored in `benchmark_*.csv` files
6. **Comparison Notebook**:
   - Side-by-side performance visualization
   - Time and memory usage summaries
   - Percentage improvements (Polars vs pandas)

---

## 📊 Conclusions

- **Polars Lazy Execution** consistently outperformed pandas and Polars Eager in both **time and memory efficiency**, especially for grouped and aggregated operations.
- **Polars Eager** also showed substantial improvements over pandas, though slightly behind its lazy counterpart.
- **Lazy Execution** allows for pipeline-level optimization, reducing redundant computation and memory allocation.
- pandas remains the most accessible for newcomers, but **Polars offers significant performance advantages** for large datasets — making it highly valuable for consultants handling high-volume data analysis.

---

## 📁 Repository Contents

```bash
├── pandas_analysis.ipynb
├── polars_eager_analysis.ipynb
├── polars_lazy_analysis.ipynb
├── libraries_comparison.ipynb
├── benchmark_pandas.csv
├── benchmark_polars_eager.csv
├── benchmark_polars_lazy.csv
└── README.md  ← you are here
