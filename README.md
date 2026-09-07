# Bank Customer Churn & Fraud Analysis

An end-to-end data analysis project exploring **customer attrition (churn)** and **transaction fraud patterns** at a retail bank, using **Python** for data cleaning and exploratory analysis, and **Power BI** for an interactive dashboard.

## 📌 Project Overview

Banks lose significant revenue when customers close their accounts. This project analyzes real customer data to answer:
- What behavioral patterns predict customer churn?
- Which customer segments are most at risk?
- What transaction patterns indicate fraud?
- Is there a relationship between fraud exposure and customer churn?

## 🗂️ Data Sources

| File | Source | Description |
|---|---|---|
| `1_bank_customers_churn_dataset.csv` | **Real data** — public dataset (Kaggle, "Credit Card Customers") | 10,127 customers with demographic and behavioral attributes |
| `2_fraud_transactions_dataset.csv` | **Synthetic data** — generated for this project | 31,201 simulated transactions linked to real customer IDs, modeled on realistic fraud patterns |

> ⚠️ **Note on data honesty:** The fraud dataset is synthetic. Real, transaction-level fraud data is either extremely large (150MB+) or inaccessible for privacy/security reasons. It was generated with realistic risk logic (merchant category, foreign transactions, time of day, distance from home) to demonstrate fraud analysis skills without compromising real data.

## 🛠️ Tools & Skills Used

- **Python** (pandas, matplotlib, seaborn) — data cleaning, exploratory data analysis (EDA)
- **Google Colab** — cloud-based analysis environment
- **Power BI** — interactive dashboard with DAX measures, relationships, and slicers
- **Statistical testing** (Chi-square test) — validating significance of findings

## 🔍 Key Findings

1. **Overall churn rate: 16.1%** of customers (1,627 out of 10,127)
2. **Transaction activity is the strongest churn signal** — churned customers transacted 35% less frequently and spent 33% less than retained customers, suggesting a gradual "wallet share erosion" before account closure
3. **Customer service contact frequency correlates strongly with churn** — customers with 4+ contacts in 12 months show churn rates 2-3x higher than those with 0-1 contacts
4. **Number of banking products is the single strongest predictor** — customers with only 1-2 products churn at ~26-28%, compared to ~10-12% for customers with 5-6 products
5. **Demographic factors (age, income) show weaker, non-linear effects** — income shows a U-shaped relationship with churn (both low and high income segments churn more than the middle tier)
6. **No reliable link found between fraud exposure and churn** in this dataset — an honest negative finding, flagged with appropriate statistical caveats (see analysis notebook)

## 📊 Dashboard Preview

![Dashboard Screenshot](Screenshot%202026-09-07%20174003.png)

The Power BI dashboard includes:
- Total customer count and churn rate KPIs
- Churn rate by number of banking products (interactive chart)
- Income category slicer for dynamic filtering

## 💡 Business Recommendations

- **Cross-sell additional products** to single-product customers — the strongest lever to reduce churn
- **Flag customers with 3+ service contacts** for proactive retention outreach
- **Monitor declining transaction activity** as an early warning signal, not just complaints

## 📁 Repository Structure

```
├── 1_bank_customers_churn_dataset.csv   # Real customer data
├── 2_fraud_transactions_dataset.csv      # Synthetic transaction data
├── bank_project_final.pbix               # Power BI dashboard file
├── Screenshot 2026-09-07 174003.png      # Dashboard preview
└── README.md
```

## 🚀 How to Explore

1. Open `bank_project_final.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop) (free) to interact with the dashboard
2. Load the CSV files into a Python/Jupyter environment to reproduce the analysis

---
*This project was built as a portfolio piece to demonstrate practical data analysis skills in banking/fintech, including data cleaning, statistical reasoning, and business storytelling.*
