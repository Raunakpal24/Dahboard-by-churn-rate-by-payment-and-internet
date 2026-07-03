# Telco Customer Churn Dashboard (Power BI)

An interactive Power BI dashboard analyzing customer churn behavior for a telecom company, built to identify which customer segments are most at risk of leaving and why.

## 📌 Project Overview

Customer churn — when a customer stops doing business with a company — is one of the most expensive problems in the subscription/telecom industry. This project analyzes 7,043 customer records to answer:

- What is the overall churn rate?
- Which customer segments churn the most?
- What factors (contract type, payment method, services used) are linked to higher churn?

## 🛠️ Tools Used

- **Power BI Desktop** — data modeling and dashboard design
- **Power Query** — data cleaning and transformation
- **DAX** — custom measures (Churn Rate, Revenue at Risk, Customer segmentation)

## 🧹 Data Cleaning

- Source: [IBM/Kaggle Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (public, 7,043 rows, 21 columns)
- Identified 11 records with blank `TotalCharges` values — all belonged to customers with `tenure = 0` (new customers not yet billed). Replaced with 0 to avoid skewing revenue calculations.
- Converted data types (TotalCharges to decimal, categorical columns to text) for accurate modeling.

## 📊 Key Insights

| Metric | Value |
|---|---|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| **Overall Churn Rate** | **26.54%** |

- **Contract type is the strongest churn driver**: Month-to-month customers churn at **42.71%**, compared to 11.27% for one-year contracts and just 2.83% for two-year contracts.
- **Payment method matters**: Customers paying via **Electronic Check churn at 45.29%** — nearly 3x higher than customers on automatic payment methods (bank transfer/credit card, ~15-17%).
- **Internet service type**: Fiber optic customers churn at a noticeably higher rate than DSL customers.

## 💡 Business Recommendation

Retention efforts should prioritize **month-to-month contract customers paying via electronic check** — this is the highest-risk segment. Offering incentives to switch to longer contracts or automatic payment methods could meaningfully reduce churn.

## 📷 Dashboard Preview

*(Add your screenshot here once uploaded, e.g.)*
`![Dashboard Screenshot](screenshots/overview.png)`

## 📁 Repository Contents

- `Telco_customer_churn_dashboard.pbix` — Power BI dashboard file
- `WA_Fn-UseC_-Telco-Customer-Churn.csv` — source dataset
- `screenshots/` — dashboard preview images

## 🔗 About

Built as a self-guided data analytics project to practice data cleaning, DAX measures, and dashboard design in Power BI.
