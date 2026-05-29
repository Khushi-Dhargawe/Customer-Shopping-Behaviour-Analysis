# Customer Shopping Behaviour Analysis

**End-to-end retail analytics pipeline · Python → PostgreSQL → Power BI · 3,900 transactions · 5 business recommendations**

> Analysed 3,900 retail transactions to uncover customer spending patterns, segment behaviour, and subscription trends — delivering actionable business recommendations through SQL queries, Python EDA, and an interactive Power BI dashboard.

---

## Why This Matters

This isn't just an EDA exercise — every query maps to a real business decision, and every insight ends with an actionable recommendation.

---

## 📌 Table of Contents
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Key Findings](#key-findings)
- [Dashboard Preview](#dashboard-preview)
- [Tools & Technologies](#tools--technologies)
- [Folder Structure](#folder-structure)
- [How to Run](#how-to-run)
- [Skills Demonstrated](#skills-demonstrated)

---

## Project Overview

A leading retail company needed to better understand its customers' shopping behaviour to improve sales, customer satisfaction, and long-term loyalty. This project delivers a complete analytics pipeline — from raw data to executive-ready insights.

**Association:** University College Cork · MSc Business Analytics

---

## Business Problem

> *"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimise marketing and product strategies?"*

The management team observed changes in purchasing patterns across demographics, product categories, and sales channels and needed data-driven answers.

---

## Dataset

| Attribute | Detail |
|-----------|--------|
| Records | 3,900 transactions |
| Columns | 18 features |
| Source | Customer transactional dataset |
| Missing data | 37 values in `review_rating` (imputed using category median) |

**Key features:** Customer ID · Age · Gender · Location · Item Purchased · Category · Purchase Amount · Season · Subscription Status · Discount Applied · Shipping Type · Review Rating · Previous Purchases

---

## Project Workflow

### 1. Data Cleaning & EDA — Python
- Loaded dataset with Pandas and profiled structure using `df.info()` and `df.describe()`
- Imputed 37 missing `review_rating` values using **category-level median**
- Renamed all columns to **snake_case** for consistency
- Feature engineering: created `age_group` (binned) and `purchase_frequency_days`
- Removed redundant `promo_code_used` column after consistency check
- Loaded cleaned DataFrame into **PostgreSQL** for SQL analysis

### 2. SQL Analysis — PostgreSQL
Answered 10 business questions using advanced SQL:

| # | Business Question | Technique Used |
|---|-------------------|----------------|
| 1 | Revenue by gender | GROUP BY · SUM |
| 2 | High-spend discount users | Subquery · WHERE filter |
| 3 | Top 5 products by rating | Aggregation · ORDER BY |
| 4 | Standard vs Express shipping spend | Conditional GROUP BY |
| 5 | Subscribers vs non-subscribers | Multi-metric aggregation |
| 6 | Most discount-dependent products | CASE · percentage calc |
| 7 | Customer segmentation | CTE · CASE WHEN |
| 8 | Top 3 products per category | CTE · Window function (ROW_NUMBER) |
| 9 | Repeat buyers & subscriptions | WHERE filter · GROUP BY |
| 10 | Revenue by age group | Derived column · GROUP BY |

### 3. Dashboard — Power BI
- Built relational data model with fact and dimension tables
- Created KPI cards: Total Customers · Avg Purchase Amount · Avg Review Rating
- Interactive slicers: Gender · Subscription Status · Category · Shipping Type
- Visuals: Revenue by Age Group · Sales by Category · Subscription breakdown

### 4. Reporting & Presentation
- Analytical report documenting all findings and methodology
- Professional presentation built in Gamma

---

## Key Findings

| Insight | Value | Business Action |
|---------|-------|-----------------|
| 💰 Male customer revenue | €157,890 | Target male segment in paid campaigns |
| 💰 Female customer revenue | €75,191 | Cross-sell opportunity vs male segment |
| 🏆 Top revenue segment | Young Adults — €62,143 | Prioritise in loyalty programme |
| 👥 Loyal customers identified | 3,116 out of 3,900 (80%) | Launch retention tier immediately |
| 📦 Highest discount-rate product | Hat — 50% of purchases discounted | Review margin impact urgently |
| ⭐ Highest-rated product | Gloves — avg rating 3.86 |
| 🚚 Express vs Standard avg spend | €60.48 vs €58.46 |

---

## Dashboard Preview

> Power BI dashboard with interactive slicers for Gender, Subscription Status, Category, and Shipping Type.

📎 Open `P1_Customer_Behavior.pbix` in Power BI Desktop to explore the full interactive dashboard.

---

## Tools & Technologies

| Category | Tools |
|----------|-------|
| Data Analysis | Python · Pandas · NumPy · Matplotlib · Seaborn |
| Development Environment | Jupyter Notebook |
| Database & Querying | PostgreSQL · SQL (CTEs · Window Functions · Subqueries) |
| Business Intelligence | Power BI · DAX · KPI Dashboards |
| Reporting | Analytical Report (PDF) · Gamma Presentation |

---

## Folder Structure

```
Customer-Shopping-Behaviour-Analysis/
│
├── Customer_Shopping_Behavior.ipynb          ← Python EDA & data cleaning notebook
├── customer_shopping_behavior.csv            ← Raw dataset
├── customer_behavior_sql.sql                 ← 10 SQL business queries (PostgreSQL)
├── P1_Customer_Behavior.pbix                 ← Power BI dashboard file
│
├── Customer_Shopping_Behavior_Analysis.pdf   ← Full analytical report
├── Business_Problem_Document.pdf             ← Business problem statement
├── Customer-Shopping-Behavior-Analysis.pptx  ← Presentation slides
│
├── requirements.txt                          ← Python dependencies
├── LICENSE                                   ← MIT License
└── README.md                                 ← Project documentation
```

---

## How to Run

**Step 1 — Clone the repository**
```bash
git clone https://github.com/Khushi-Dhargawe/Customer-Shopping-Behaviour-Analysis.git
cd Customer-Shopping-Behaviour-Analysis
```

**Step 2 — Install Python dependencies**
```bash
pip install -r requirements.txt
```

**Step 3 — Run the Python notebook**

Open `Customer_Shopping_Behavior.ipynb` in Jupyter Notebook and run all cells to:
- Load and profile the dataset
- Perform EDA and visualisations
- Clean and transform the data
- Export cleaned data to PostgreSQL

**Step 4 — Run SQL queries**

Load the cleaned CSV into PostgreSQL, then open and execute `customer_behavior_sql.sql`.

**Step 5 — Explore the dashboard**

Open `P1_Customer_Behavior.pbix` in Power BI Desktop and refresh the data source.

---

## What I'd Do With More Data

With transactional timestamps I'd build a cohort retention analysis. With product margin data I'd calculate true profitability by segment, not just revenue.

---

## Skills Demonstrated

`Data Analysis` `Business Analysis` `Python` `Pandas` `NumPy` `SQL` `PostgreSQL`
`Power BI` `DAX` `EDA` `Feature Engineering` `Data Cleaning` `Data Visualisation`
`Customer Segmentation` `Reporting` `Data Storytelling` `Stakeholder Communication`

---

## Business Recommendations

1. **Boost subscriptions** — only 27% of customers subscribe; promote exclusive subscriber benefits
2. **Loyalty programme** — reward the 3,116 loyal customers to reduce churn risk
3. **Discount policy review** — Hat, Sneakers, Coat have 48–50% discount rates; assess margin impact
4. **Targeted marketing** — Young Adults (€62,143) and Express shipping users are the highest-value segments
5. **Product focus** — Highlight Gloves, Sandals, Boots in campaigns based on top review ratings

---

*Project completed as part of MSc Business Analytics — University College Cork*

*Connect with me on [LinkedIn](https://www.linkedin.com/in/khushi-dhargawe/)*