# OTT Customer Churn & Retention Analysis

SQL and Python analysis of OTT customer churn, retention risk, and revenue impact.

## 📌 Project Overview

This project analyzes customer, subscription, and support data from an OTT platform to identify churn patterns, evaluate revenue impact, and identify customer segments that require retention attention.

The analysis combines relational data extraction using SQLite/SQL with Python-based data cleaning, feature engineering, exploratory data analysis, visualization, and business interpretation.

##  Business Objective

The key objectives of this analysis are to:

- Measure overall customer churn and retention.
- Identify subscription plans and contract types associated with higher churn.
- Analyze churn patterns across geography and time.
- Examine the relationship between customer support escalations and churn.
- Quantify the revenue and estimated CLTV impact of customer churn.
- Segment customers based on churn risk to support retention prioritization.

##  Dataset

The project uses a raw OTT customer dataset containing subscription, customer, churn, complaint, and revenue-related information.

The dataset includes:

- Customer and subscription details
- Subscription start and cancellation dates
- Subscription type, plan type, and contract type
- Monthly charges and customer lifetime value (CLTV)
- Customer complaints and escalation information
- Customer demographic and location details

The original raw dataset is stored separately in the `data/` folder to preserve the source data and support reproducibility.

**Dataset file:** `data/customer_churn_data_raw.xlsx`

##  Tech Stack

- **Python**
- **SQL**
- **SQLite**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

##  Analytical Workflow

1. **Data Setup**
   - Imported raw customer data and created a SQLite database.
   - Worked with separate customer, subscription, and support tables.

2. **Relational Data Extraction**
   - Connected SQLite with Python using `sqlite3`.
   - Extracted data into Pandas DataFrames using SQL queries.

3. **Data Cleaning & Quality Checks**
   - Renamed and removed unnecessary columns.
   - Checked data types, duplicates, unique values, and missing values.
   - Standardized data and handled missing country information.
   - Converted relevant date fields to datetime format.

4. **Data Integration**
   - Aggregated customer support complaints.
   - Combined customer, subscription, and support information at the customer level.

5. **Feature Engineering**
   - Created a **churn flag** based on customer cancellation status.
   - Calculated **customer tenure in days** using subscription and cancellation dates.
   - Aggregated **complaint counts per customer** from support data.
   - Created **churn-risk segments (Low, Medium, High)** using customer churn scores.
   - Derived **cancellation month** to analyze monthly churn trends.
   - Calculated **ARPU, revenue at risk, revenue loss percentage, and estimated CLTV lost** to quantify the financial impact of churn.

6. **Exploratory Data Analysis**
   - Analyzed churn by subscription plan, contract type, geography, and month.
   - Used aggregation, group-by analysis, and pivot tables.

7. **Visualization**
   - Created visualizations using Matplotlib and Seaborn to identify behavioral and churn patterns.

8. **Business Insights & Recommendations**
   - Translated analytical findings into actionable customer retention recommendations.

##  Key KPIs

| KPI | Result |
|---|---:|
| Overall Churn Rate | **28.57%** |
| Retention Rate | **71.43%** |
| Monthly Contract Churn | **55.6%** |
| Annual Contract Churn | **8.3%** |
| Basic Plan Churn | **60%** |
| ARPU | **₹18.85** |
| Total Revenue | **₹395.79** |
| Revenue at Risk | **₹73.94** |
| Revenue Loss | **18.68%** |
| Estimated CLTV Lost | **2,047** |
| Average Tenure | **1,527 days** |
| Support Escalation Rate | **19.05%** |

##  Key Findings

### 1. Monthly subscribers show higher churn risk

Monthly subscribers had a **55.6% churn rate**, compared with **8.3% for annual subscribers**, against an overall churn rate of 28.57%.

This identifies monthly contracts as an important segment for retention analysis.

### 2. Basic plan has the highest observed churn

The Basic subscription plan recorded the highest observed churn rate at **60%**, compared with 22.22% for Standard and 14.29% for Premium.

Although the Basic plan has the highest churn rate, its lower ARPU limits its immediate revenue impact relative to higher-value segments.

### 3. Churn has a measurable revenue impact

The analysis estimates approximately **₹73.94 in revenue at risk**, representing **18.68% of total revenue**, along with an estimated **CLTV loss of 2,047**.

### 4. Churn varies across time and geography

**September 2024** recorded the highest number of churned customers in the dataset.

Karnataka and Meghalaya recorded the highest number of churned customers, with **2 churned customers each**.

These patterns warrant further investigation into potential pricing, service, customer-support, or competitive factors.

### 5. Support escalations and churn

The analysis observed a **0.77 correlation between support escalations and churn**, suggesting that customers experiencing support-related issues may warrant closer retention monitoring.

Correlation does not establish causation, so this relationship should be investigated further using additional customer-support and behavioral data.

##  Business Recommendations

Based on the analysis:

- Investigate the significantly higher churn among **monthly subscribers** and evaluate pricing, engagement, and plan-value factors.
- Review the **Basic plan's value proposition** and understand why it has the highest observed churn.
- Investigate the **September 2024 churn spike**, particularly across the most affected regions.
- Examine customer complaints, technical issues, pricing changes, and competitor activity as potential contributors to regional or monthly churn patterns.
- Prioritize **high-risk, high-value customers** for proactive retention efforts.
- Use customer support history and complaint activity as additional signals when prioritizing retention outreach.

##  Project File

- `OTT_Customer_Churn_Analysis.ipynb` — Complete SQL and Python analysis, including data extraction, cleaning, feature engineering, EDA, visualization, and business insights.

##  Key Skills Demonstrated

**SQL | Python | SQLite | Data Cleaning | Data Integration | Feature Engineering | Exploratory Data Analysis | Data Visualization | Customer Churn Analysis | Business Analytics**
