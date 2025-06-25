📊 Customer Insights Analysis in Tableau

This project provides a comprehensive customer behavior analysis using Tableau Public. It visualizes customer churn, satisfaction levels, gender distribution, and average monthly spend. The goal is to help stakeholders understand retention drivers and improve service strategies.

📌 Objective

To analyze key customer metrics and generate visual insights for:

Churned vs. retained customers

Satisfaction score patterns

Monthly spending behavior

Demographic breakdown by gender

📊 Dashboard Components

1. Satisfaction Score

A matrix view that shows the average and sum of customer satisfaction ratings.

Metrics used:

AVG([Satisfaction Score])

SUM([Satisfaction Score])

2. Average Spend Analysis

A simple bar chart displaying average monthly spend.

Metric used:

AVG([Monthly Spend])

3. Customer Churn Overview

A bar graph showing the number of customers who churned vs. retained.

Metrics used:

CNTD([Customer ID])

Dimension:

Churned field (Yes/No)

4. Gender Distribution

Pie chart showing the gender split across the customer base.

Metrics used:

SUM([Satisfaction Score]) (used for size/angle)

Dimension:

Gender (M/F)

⚙️ Queries and Calculations

Below are key Tableau calculated fields and aggregations used in the visualizations:

✅ Churn Count

CNTD([Customer ID])

✅ Average Satisfaction Score

AVG([Satisfaction Score])

✅ Monthly Spend Average

AVG([Monthly Spend])

✅ Churn Rate (if custom calc created)

SUM(IF [Churned] = 'Yes' THEN 1 ELSE 0 END) / COUNT([Customer ID])

🧩 Challenges Faced

During the development of this Tableau dashboard, several challenges were encountered:

Data Cleaning & Formatting: The original dataset contained inconsistent values and missing entries, which required preprocessing outside Tableau before loading.

Granularity Issues: Aggregating satisfaction scores and spending metrics while preserving individual-level insights required careful design of visualizations and filters.

Balancing Detail and Clarity: Achieving the right balance between detail and simplicity in the dashboards was essential to maintain readability for stakeholders.

Dynamic Filtering: Implementing filters that interacted across multiple sheets sometimes led to performance issues and required optimization.

Churn Logic Validation: Ensuring the accuracy of churn identification logic (e.g., interpreting "Churned" status) needed validation against the original business rules.

🧠 Key Insights

Average Monthly Spend: $171.4

Balanced churn vs. retention

Even satisfaction score distribution

Gender distribution nearly equal

🗂️ File Structure

File

Description

Screenshot.png

Final dashboard image

.twb / .twbx

Tableau workbook file

dataset.csv

Customer data (not shared here)

🧪 How to Use

Clone this repo

Open Tableau Public or Tableau Desktop

Load the dataset (.csv)

Use the sheets:

Satisfaction Score

Churn Overview

Spend Analysis

Gender Review

Customize or publish to Tableau Public

💬 Contact

Created by @Shruti29044📧 Open to feedback, collaboration, or improvements!
