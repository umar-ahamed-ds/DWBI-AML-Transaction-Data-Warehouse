# 💳 AML Transaction Data Warehouse & BI System

🚀 End-to-End Data Warehousing & Business Intelligence Project

Built using SQL Server, SSIS, SSAS, Excel, and Power BI

---

## 📌 Project Overview

This project implements a complete **Data Warehouse and Business Intelligence (DWBI) solution** based on a **Synthetic Transaction Monitoring Dataset for Anti-Money Laundering (AML)** sourced from Kaggle.

The goal is to transform raw financial transaction data into structured, analyzable insights to support decision-making and fraud detection analysis.

---

## 🏗️ Architecture

**Data Sources (OLTP + CSV + Excel + SQL)** → **Staging Layer** → **Data Warehouse (Star Schema)** → **BI Layer (SSAS, Excel, Power BI)**

---

## ⭐ Key Features

### 📊 Data Warehouse Design

* Star Schema implementation

* **Fact Table:** `Fact_Transactions`

* **Dimension Tables:**

  * `Dim_Date`
  * `Dim_Account` *(Role-playing: Sender & Receiver)*
  * `Dim_Location` *(SCD Type 2)*
  * `Dim_Currency`
  * `Dim_PaymentType`

---

### 🔄 ETL Process (SSIS)

* Integrated multiple data sources (Database + CSV files)
* Data cleansing and transformation
* Lookup transformations for surrogate key mapping
* Derived columns for calculated attributes
* Data type conversion and validation

📌 Implemented **Slowly Changing Dimension Type 2 (SCD Type 2)** to track historical changes in location data

---

### ⏳ Advanced Concept

#### Accumulating Fact Table

Tracks transaction lifecycle:

* Transaction creation time
* Transaction completion time
* Processing duration (hours)

---

### 🧠 OLAP Cube (SSAS)

* Built multidimensional cube

**Measures:**

* Total Transaction Amount
* Transaction Count

**Hierarchies:**

* Date (Year → Quarter → Month → Day)
* Location (Country → City)

---

### 📈 Analytics & Reporting

Performed OLAP operations:

* Roll-up
* Drill-down
* Slice
* Dice
* Pivot

---

### 📊 Power BI Dashboard

* KPI Cards (Total Transactions, Total Amount)
* Charts (Transactions by Location, Payment Type)
* Matrix Visual for detailed insights
* Slicers for interactive filtering

---

## 🛠️ Tech Stack

* Microsoft SQL Server
* SSIS (ETL)
* SSAS (OLAP Cube)
* Power BI
* Excel (Pivot Tables & OLAP Analysis)

---

## 🔗 Dataset Source

The selected dataset is the **Synthetic Transaction Monitoring Dataset for Anti-Money Laundering (AML)** available on Kaggle.

This dataset simulates realistic financial transactions between accounts and includes attributes useful for analyzing suspicious financial behavior, such as:

* Sender and receiver account details
* Transaction amount and currency
* Payment type
* Geographic location
* Transaction timestamps

📊 It is well-suited for building **data warehouse models**, performing **ETL processes**, and conducting **analytical reporting** for fraud detection and monitoring.

🔗 Dataset Link:
https://www.kaggle.com/datasets/berkanoztas/synthetic-transaction-monitoring-datasetaml/

---

## 💡 Key Learnings

* End-to-end Data Warehouse architecture design
* ETL pipeline development using SSIS
* Handling Slowly Changing Dimensions (SCD Type 2)
* Accumulating fact table implementation
* OLAP cube design and multidimensional analysis
* Data visualization using Power BI

---

## 👩‍💻 Author

**Your Name**
BSc (Hons) in IT – Data Science
