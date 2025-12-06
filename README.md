# vistora_project
---

## 🎯 Assignment Objective

The goal of this assignment is to understand how **feature engineering works in real-world scenarios**, particularly how:

- Data is **stored and queried from Snowflake**
- Raw data is **transformed into ML-ready features**
- Features are **stored in a centralized Feature Store**
- These features are then **used in machine learning models**

This project demonstrates an **end-to-end SQL-based feature engineering pipeline** implemented entirely within the **Snowflake Data Platform**.

---

## 1️⃣ Introduction to Feature Engineering

### ✅ What is Feature Engineering?

**Feature Engineering** is the process of:
> Transforming raw data into meaningful input features that improve the performance of machine learning models.

In simple terms:
- Raw data → is often messy and not directly usable
- Feature engineering → converts it into **useful numeric signals**
- Machine learning models → learn patterns from these signals

Example:
- Raw Data: `transaction_timestamp`
- Engineered Feature: `number_of_transactions_last_30_days`

---

### ✅ Why is Feature Engineering Important?

Feature engineering is important because:

- ✅ It significantly **improves model accuracy**
- ✅ Helps models **learn patterns faster**
- ✅ Reduces **noise and irrelevant information**
- ✅ Makes models **generalize better**
- ✅ Converts business data into **mathematical form**

Many ML experts agree:
> **Better features often matter more than better algorithms.**

---

### ✅ Types of Feature Engineering Techniques

| Technique | Description | Example |
|----------|-------------|---------|
| **Normalization / Scaling** | Converts values to the same range | Min-Max Scaling |
| **Encoding** | Converts categorical data into numeric | One-hot encoding |
| **Aggregation** | Combine multiple rows into one feature | Monthly transaction total |
| **Time-based Features** | Extract temporal patterns | Day of week, Recency |
| **Boolean Flags** | True/False behavior detection | Active customer flag |
| **Frequency Encoding** | Count-based encoding | Country frequency |

✅ In this project, the following techniques are used:
- Time-based aggregation (`TX_COUNT_30D`)
- Boolean flags (`IS_ACTIVE_30D`)
- Numeric aggregations (`TX_SUM_30D`, `TX_AVG_30D`)
- Frequency encoding (`COUNTRY_TX_COUNT`)
- Recency calculation (`DAYS_SINCE_LAST_TX`)

---

## 2️⃣ Using Snowflake for Data Storage & Processing

### ✅ How Snowflake is Used

Snowflake is a **cloud-based data platform** used for:

- ✅ Storing large volumes of **structured data**
- ✅ Processing data using **high-performance SQL**
- ✅ Separating **compute and storage**
- ✅ Supporting **analytics and machine learning workflows**

In this project, Snowflake stores:
- Customer profile data
- Transaction history
- Feature store tables
- Training datasets

