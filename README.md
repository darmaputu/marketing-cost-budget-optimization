# 📊 Marketing Cost Budget Optimization

## 📌 Overview

This project analyzes customer behavior, sales performance, marketing costs, customer acquisition, and return on marketing investment to support marketing budget optimization.

The analysis combines website visit data, order transactions, and marketing cost data to understand how customers interact with the product, when they make purchases, how much they contribute in revenue, and how efficiently different marketing sources acquire customers.

---

## 🎯 Business Objective

The main objectives of this project are to:

* Understand user activity and engagement patterns.
* Analyze customer purchasing behavior.
* Measure customer retention and repeat usage.
* Identify when customers make their first purchase.
* Analyze order volume and revenue trends.
* Calculate Customer Lifetime Value (LTV).
* Evaluate marketing spending by acquisition source.
* Calculate Customer Acquisition Cost (CAC).
* Evaluate return on marketing investment using the project's ROI metric.
* Provide data-driven insights for marketing budget optimization.

---

## 📂 Dataset

The analysis uses three datasets:

### 1. Visits Data

`visits_log_us.csv`

Contains information about user sessions and website visits.

Key variables include:

* `device`
* `start_ts`
* `end_ts`
* `source_id`
* `uid`

The original dataset contained **359,400 visit records**. Two records with invalid session times were removed, resulting in **359,398 valid records**.

### 2. Orders Data

`orders_log_us.csv`

Contains customer purchase transactions.

Key variables:

* `buy_ts`
* `revenue`
* `uid`

The dataset contains **50,415 order transactions**.

### 3. Marketing Costs Data

`costs_us.csv`

Contains daily marketing spending by acquisition source.

Key variables:

* `source_id`
* `dt`
* `costs`

The dataset contains **2,542 marketing cost records**.

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Seaborn
* Exploratory Data Analysis
* Cohort Analysis
* Retention Analysis
* Customer Lifetime Value (LTV)
* Customer Acquisition Cost (CAC)
* ROI Analysis

---

## 🔍 Data Preparation

The following data preparation steps were performed:

* Imported the visits, orders, and marketing cost datasets.
* Standardized column names.
* Converted timestamp columns into datetime format.
* Identified and removed invalid visit records where the session end time occurred before the start time.
* Created daily, weekly, and monthly time dimensions.
* Created customer first-visit and first-purchase dates.
* Combined customer visit and purchase information for behavioral analysis.
* Prepared marketing cost data for monthly and source-level analysis.

---

## 👥 Product & User Behavior Analysis

The project analyzes user activity across different time periods.

### Average Users

| Metric        | Average Users |
| ------------- | ------------: |
| Daily Users   |           907 |
| Weekly Users  |         5,724 |
| Monthly Users |        23,228 |

The analysis also shows that user activity was highest toward the end of the year, particularly in November and December.

### Sessions per User

Session activity was analyzed by comparing the number of sessions with the number of unique users per day.

The highest sessions-per-user ratio occurred on **November 24**, reaching approximately **1.217 sessions per user**.

---

## ⏱️ Session Duration Analysis

User session duration was calculated from the difference between session start and end timestamps.

### Session Duration Statistics

| Metric  |          Value |
| ------- | -------------: |
| Average | 643.04 seconds |
| Median  |    300 seconds |
| Mode    |     60 seconds |
| Maximum | 42,660 seconds |

The distribution shows that most sessions were relatively short, while a smaller number of sessions had significantly longer durations.

---

## 🔄 Customer Retention Analysis

Customer cohorts were created based on the month of the customer's first visit.

Retention was calculated by tracking how many users continued to return after their initial visit.

The analysis found that the average percentage of users returning after their first visit was approximately **5.36%**.

---

## 🛒 Purchase Behavior Analysis

The project analyzes the time between a customer's first website visit and their first purchase.

### Key Finding

Most customers made their first purchase on **day 0**, meaning within 24 hours of their first visit. The next largest group made their first purchase on the following day.

### Order Behavior

Customer order behavior was aggregated by:

* Number of transactions
* Total revenue
* Monthly order activity
* Customer cohorts

Across customers, the average number of transactions was approximately **1.38**, while the average revenue per transaction was approximately **6.90**.

The highest transaction volume and revenue occurred in **December**, followed by October.

---

## 💰 Customer Lifetime Value (LTV)

Customer cohorts were created based on the month of their first purchase.

LTV was calculated based on customer revenue relative to the number of buyers within each cohort.

The analysis applied a **50% margin rate** when calculating gross profit within the cohort analysis.

### LTV Findings

* Average LTV over the analyzed six-month period: **0.36**
* Average LTV for the same-month period: **0.26**

The cohort analysis shows how customer value changes as customers continue purchasing after their initial acquisition.

---

## 📣 Marketing Cost Analysis

Marketing spending was analyzed by month and acquisition source.

### Total Marketing Cost

The project recorded total marketing spending across the analyzed period and examined how spending changed over time.

The highest monthly marketing expenditure occurred in **December**.

### Marketing Cost by Source

| Source    | Marketing Cost |
| --------- | -------------: |
| Source 1  |      20,833.27 |
| Source 2  |      42,806.04 |
| Source 3  |     141,321.63 |
| Source 4  |      61,073.60 |
| Source 5  |      51,757.10 |
| Source 9  |       5,517.49 |
| Source 10 |       5,822.49 |

**Source 3** accounted for the largest marketing expenditure at **141,321.63**.

---

## 💵 Customer Acquisition Cost (CAC)

Customer Acquisition Cost was calculated by comparing marketing costs with the number of newly acquired buyers.

The overall average CAC calculated in the project was:

**Average CAC = 9.01**

### CAC by Marketing Source

| Source    | Average CAC |
| --------- | ----------: |
| Source 1  |        9.49 |
| Source 2  |       16.29 |
| Source 3  |       15.58 |
| Source 4  |        7.27 |
| Source 5  |        8.34 |
| Source 9  |        6.84 |
| Source 10 |        6.56 |

Source 2 had the highest average CAC at **16.29**, indicating a higher acquisition cost per new customer compared with the other analyzed sources.

An important observation from the analysis is that the source with the highest marketing expenditure was not necessarily the source with the highest CAC.

---

## 📈 ROI Analysis

The project evaluates ROI using the relationship between customer LTV and CAC.

The analysis calculates:

```text
CAC = Marketing Cost / Number of New Buyers

ROI = LTV / CAC
```

ROI was then analyzed cumulatively across customer cohorts and customer age in months.

The cohort analysis shows that ROI changes over time as customers generate additional revenue after their initial acquisition. Some cohorts reached a cumulative ROI above **1.0**, while others remained below 1.0 during the observed period.

---

## 💡 Key Findings

1. Average daily, weekly, and monthly users were **907, 5,724, and 23,228**, respectively.

2. User activity was highest toward the end of the year, particularly in November and December.

3. The highest sessions-per-user ratio occurred on **November 24**, at approximately **1.217 sessions per user**.

4. The average returning-user rate after the first visit was approximately **5.36%**.

5. Most customers made their first purchase within **24 hours of their first visit**.

6. December recorded the highest transaction volume and revenue.

7. **Source 3** had the highest marketing expenditure at **141,321.63**.

8. **Source 2** had the highest average CAC at **16.29**.

9. The overall average CAC was **9.01**.

10. The analysis demonstrates that marketing spend, customer acquisition cost, customer lifetime value, and ROI should be evaluated together when analyzing marketing efficiency.

---

## 🔄 Analytical Workflow

```text
Raw Data
   ↓
Data Cleaning & Validation
   ↓
User & Session Analysis
   ↓
Customer Purchase Analysis
   ↓
Cohort & Retention Analysis
   ↓
LTV Calculation
   ↓
Marketing Cost Analysis
   ↓
CAC Calculation
   ↓
ROI Analysis
   ↓
Marketing Budget Insights
```

---

## 💼 Business Value

This project demonstrates how customer and marketing data can be combined to evaluate:

* User engagement
* Customer retention
* Purchase behavior
* Revenue performance
* Customer Lifetime Value
* Marketing spending
* Customer Acquisition Cost
* Marketing ROI
* Acquisition source efficiency

The analysis provides a framework for evaluating marketing budget allocation based on both acquisition cost and customer value rather than marketing expenditure alone.

---

## 📁 Project Structure

```text
├── README.md
├── Marketing Cost Budget Optimization.ipynb
└── dataset/
    ├── visits_log_us.csv
    ├── orders_log_us.csv
    └── costs_us.csv
```

---

## 👤 Author

**I Putu Darma Ruswara**

Data Analyst | Business Analytics & Data Governance
