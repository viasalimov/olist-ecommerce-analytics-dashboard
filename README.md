# Olist E-Commerce Analytics Dashboard

End-to-end Power BI analytics project focused on revenue analysis, logistics performance, and customer satisfaction using the Olist Brazilian E-Commerce Public Dataset.

---

# Project Overview

This project analyzes Brazilian e-commerce marketplace data from Olist to explore:
- sales and revenue trends
- product category performance
- customer satisfaction
- delivery efficiency
- freight costs
- operational performance

The goal of the project was to build an interactive business intelligence dashboard capable of generating meaningful operational and customer insights through analytics and visualization.

---

# Tech Stack

- Power BI
- Power Query
- DAX
- Data Modeling
- Snowflake Schema
- Business Analytics
- Data Visualization

---

# Key KPIs

- Total Revenue: R$15.84M
- Total Orders: 99K
- Average Delivery Time: 12.50 Days
- Average Review Score: 4.09 / 5
- Total Freight: R$2.25M

---

# Dashboard Features

The dashboard includes:
- KPI cards
- Monthly Revenue Trend
- Top Product Categories by Revenue
- Review Score vs Average Delivery Days
- Delivery Time vs Customer Satisfaction scatter plot
- Interactive slicers:
  - Date
  - Product Category
  - Order Status
  - Review Score

---

# Dashboard Preview

![Dashboard Overview](screenshots/dashboard-overview.png)

---

# Key Insights

- Longer delivery times were generally associated with lower customer review scores.
- Product category performance varied significantly across the marketplace.
- Revenue trends showed strong seasonal fluctuations.
- Freight costs represented a significant operational expense.
- Customer satisfaction was strongly influenced by logistics performance.

---

# Delivery Time vs Customer Satisfaction

The scatter plot visualization was used to analyze the relationship between delivery speed and customer satisfaction.

A trendline was added to identify the correlation between:
- average delivery days
- average review scores

The analysis showed that longer delivery times generally resulted in lower customer review scores.

![Scatter Plot](screenshots/scatterplot.png)

---

# Data Modeling

A Snowflake schema was implemented because the dataset contains multiple fact tables:
- order_items
- order_payments
- order_reviews

Using a simple Star Schema would create:
- many-to-many relationship issues
- duplicated data
- inaccurate aggregations

The Snowflake structure reduced duplication and improved analytical flexibility.

Cross-filter direction was configured as "Both" between:
- order_items ↔ orders
- order_reviews ↔ orders

This ensured slicers such as:
- Product Category
- Review Score

properly propagated across all visuals and KPIs.

![Data Model](screenshots/data-model.png)

---

# Data Preparation & DAX

Data preparation included:
- renaming tables for clarity
- removing unnecessary columns
- validating primary key uniqueness
- adjusting date formats for dynamic time analysis
- handling blank category values

Main DAX functions used:
- DISTINCTCOUNT
- SUMX
- AVGX
- DATEDIFF

Measures created:
- Total Orders
- Total Revenue
- Total Freight
- Average Delivery Days
- Average Review Score

---

# Additional Analytical Considerations

To better align Total Payments with Total Revenue, filters were applied to the following order statuses:
- delivered
- approved
- shipped

This reduced discrepancies caused by cancelled and incomplete orders.

Some minor inconsistencies remained due to missing payment records for several shipped orders.

---

# Summary & Data Modeling Page

The project also includes a dedicated summary page explaining:
- schema selection
- relationship logic
- filter propagation
- DAX calculations
- modeling decisions

![Summary Page](screenshots/summary-page.png)

---

# Power BI Dashboard File

Due to GitHub file size limitations, the Power BI dashboard file is available via Google Drive:

[Download Power BI Dashboard](https://drive.google.com/file/d/1FZZG0hr8kXeUDFX7P3WUy-5FYMhCAJxh/view?usp=sharing)

---

# Repository Structure

```text
dashboard/     -> Power BI dashboard (.pbix)
report/        -> PDF & HTML analytics reports
screenshots/   -> Dashboard screenshots
data/          -> Dataset source information
```

---

# Project Files

Included in this repository:
- Power BI Dashboard (.pbix via Google Drive)
- PDF Analytics Report
- HTML Report
- Dashboard Screenshots

---

# Dataset

Dataset: Brazilian E-Commerce Public Dataset by Olist

Source:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Period:
2016–2018

Dataset size:
~100,000 orders

---

# Skills Demonstrated

- Power BI Dashboard Development
- DAX Calculations
- Data Modeling
- Snowflake Schema Design
- Filter Propagation Logic
- Business Analytics
- E-Commerce Analytics
- Data Visualization
- Analytical Storytelling

---

# Author

Alikhan Salimov

Management & AI Student at LUISS University  
Interested in Data Analytics, Product Analytics, AI, and Business Intelligence.
