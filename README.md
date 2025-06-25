# 📊 Customer Insights Analysis in Tableau

This project provides a comprehensive customer behavior analysis using **Tableau Public**. It visualizes customer churn, satisfaction levels, gender distribution, and average monthly spend. The goal is to help stakeholders understand retention drivers and improve service strategies.

---

## 📌 Objective

To analyze key customer metrics and generate visual insights for:

- Churned vs. retained customers
- Satisfaction score patterns
- Monthly spending behavior
- Demographic breakdown by gender

---

## 📊 Dashboard Components

### 1. Satisfaction Score
- Matrix view showing average and total satisfaction ratings.
- **Metrics**:
  - `AVG([Satisfaction Score])`
  - `SUM([Satisfaction Score])`

### 2. Average Spend Analysis
- Bar chart displaying average monthly spend per customer.
- **Metric**:
  - `AVG([Monthly Spend])`

### 3. Customer Churn Overview
- Bar graph showing churned vs. retained customer count.
- **Metric**:
  - `CNTD([Customer ID])`
- **Dimension**:
  - `Churned` (Yes/No)

### 4. Gender Distribution
- Pie chart showing gender split.
- **Metric**:
  - `SUM([Satisfaction Score])`
- **Dimension**:
  - `Gender` (M/F)

---

## ⚙️ Key Calculations Used

```tableau
-- Churn Count
CNTD([Customer ID])

-- Average Satisfaction Score
AVG([Satisfaction Score])

-- Average Monthly Spend
AVG([Monthly Spend])

-- Churn Rate (if created)
SUM(IF [Churned] = 'Yes' THEN 1 ELSE 0 END) / COUNT([Customer ID])`

##  Challenges Faced
During the development of this Tableau dashboard, several challenges were encountered:

Data Cleaning & Formatting: The original dataset contained inconsistent values and missing entries, which required preprocessing outside Tableau before loading.

Granularity Issues: Aggregating satisfaction scores and spending metrics while preserving individual-level insights required careful design of visualizations and filters.

Balancing Detail and Clarity: Achieving the right balance between detail and simplicity in the dashboards was essential to maintain readability for stakeholders.

Dynamic Filtering: Implementing filters that interacted across multiple sheets sometimes led to performance issues and required optimization.

Churn Logic Validation: Ensuring the accuracy of churn identification logic (e.g., interpreting "Churned" status) needed validation against the original business rules.

