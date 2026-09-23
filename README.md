# Superstore Sales & Profitability Analytics with AI-Assisted Transaction Anomaly Detection

---

## Project Overview

This project performs a comprehensive end-to-end data analytics study on the Seven 11 Superstore
transactional sales dataset. It combines traditional Exploratory Data Analysis (EDA) with an
AI-powered anomaly detection pipeline using Isolation Forest to identify unusual or suspicious
transactions, delivering actionable business intelligence for retail management decisions.

---

## Dataset

| Property       | Detail                                  |
|----------------|-----------------------------------------|
| **File**       | `Seven 11 Superstore.csv`               |
| **Rows**       | 9,994 transactions                      |
| **Columns**    | 21                                      |
| **Time Range** | 2014 – 2017                             |
| **Geography**  | United States (4 regions)               |

### Columns

| Column         | Description                              |
|----------------|------------------------------------------|
| Row ID         | Unique row number                        |
| Order ID       | Order identifier (multiple items/order)  |
| Order Date     | Date the order was placed                |
| Ship Date      | Date the order was shipped               |
| Ship Mode      | Shipping method (4 options)              |
| Customer ID    | Unique customer identifier               |
| Customer Name  | Customer full name                       |
| Segment        | Consumer / Corporate / Home Office       |
| Country        | Country (all United States)              |
| City           | City of delivery                         |
| State          | State of delivery                        |
| Postal Code    | Delivery postal code                     |
| Region         | East / West / Central / South            |
| Product ID     | Unique product identifier                |
| Category       | Furniture / Office Supplies / Technology |
| Sub-Category   | 17 product sub-categories                |
| Product Name   | Full product name                        |
| Sales          | Revenue for line item (USD)              |
| Quantity       | Units ordered                            |
| Discount       | Discount applied (0.0 – 0.8)            |
| Profit         | Profit for line item (USD, can be < 0)  |

---

## Project Structure

```
IBM_SkillBuild_Superstore_Project/
│
├── Seven 11 Superstore.csv          ← Raw dataset
├── Superstore_Analytics.ipynb       ← Main analysis notebook (31 sections)
├── requirements.txt                 ← Python package dependencies
└── README.md                        ← This file
```

---

## Notebook Sections

| # | Section |
|---|---------|
| 0 | Project Title & Header |
| 1 | Library Imports & Configuration |
| 2 | Dataset Loading |
| 3 | Data Understanding |
| 4 | Data Quality Checks |
| 5 | Missing Value Analysis |
| 6 | Duplicate Analysis |
| 7 | Data Type Validation |
| 8 | Date Conversion |
| 9 | Feature Engineering |
| 10 | Exploratory Data Analysis |
| 11 | KPI Analysis |
| 12 | Sales Analysis |
| 13 | Profit Analysis |
| 14 | Profit Margin Analysis |
| 15 | Category Analysis |
| 16 | Sub-Category Analysis |
| 17 | Regional Analysis |
| 18 | Customer Analysis |
| 19 | Product Analysis |
| 20 | Segment Analysis |
| 21 | Monthly Sales Trend |
| 22 | Monthly Profit Trend |
| 23 | Discount vs Profit Analysis |
| 24 | Loss-Making Transactions & Orders |
| 25 | Top Customers |
| 26 | Top Products |
| 27 | AI Anomaly Detection — Isolation Forest |
| 28 | Anomaly Visualization |
| 29 | Business Insights |
| 30 | Business Recommendations |
| 31 | Final Conclusion |

---

## Setup & Installation

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 3. Open the notebook

Open `Superstore_Analytics.ipynb` in the Jupyter interface and run all cells top-to-bottom
(**Kernel → Restart & Run All**).

---

## AI Methodology

**Algorithm:** Isolation Forest (`sklearn.ensemble.IsolationForest`)

| Parameter       | Value                  |
|-----------------|------------------------|
| contamination   | 0.05 (5% anomaly rate) |
| random_state    | 42                     |
| n_estimators    | 100                    |

**Input Features:** `Sales`, `Quantity`, `Discount`, `Profit`

Isolation Forest is an unsupervised tree-based algorithm that isolates observations by randomly
selecting features and split values. Anomalies — transactions with unusual combinations of
sales, quantity, discount, and profit — are isolated in fewer splits and receive a score of `-1`.

---

## Libraries Used

| Library       | Version  | Purpose                        |
|---------------|----------|--------------------------------|
| pandas        | ≥ 1.5.0  | Data manipulation & analysis   |
| numpy         | ≥ 1.23.0 | Numerical operations           |
| matplotlib    | ≥ 3.6.0  | All data visualizations        |
| scikit-learn  | ≥ 1.1.0  | Isolation Forest, StandardScaler |
| jupyter       | ≥ 1.0.0  | Notebook runtime               |

---


---
