# Project: Coca-Cola Sales Performance Dashboard

## Table of Contents  
1. [Introduction](#introduction)  
2. [Data Acquisition and Preparation](#data-acquisition-and-preparation)  
3. [Data Cleaning](#data-cleaning)  
4. [Data Processing](#data-processing)  
5. [Data Analysis and Visualization](#data-analysis-and-visualization)  
6. [Data Interpretation](#data-interpretation)  
7. [Recommendations](#recommendations)  

---

## Introduction  
This project provides an in-depth analysis of the **Coca-Cola Sales Performance Dashboard** for 2022. It showcases data across multiple business dimensions, including geography, retail channels, delivery methods, and product performance.

Key business questions addressed:
- What is the distribution of sales and profit across retailers and regions?
- Which delivery companies and cities contribute most to volume?
- How are prices, margins, and total revenue trending?
- How close is the business to meeting its revenue and quantity targets?

---

## Data Acquisition and Preparation  
The dashboard data was structured using the following fields:

`Retailer`, `Retailer ID`, `Invoice Date`, `Region`, `State`, `City`, `Beverage Brand`, `"Days to Deliver"`, `"Delivery Company"`, `"Price per Unit"`, `Units Sold`, `Total Sales`, `Operating Profit`, `Operating Margin`

Data was extracted from interactive Power BI dashboards representing Coca-Cola's operations across the U.S. in 2022.

---

## Data Cleaning  
The following data cleaning procedures were applied:
- Standardized date format in the `Invoice Date` column.
- Cleaned and formatted `Price per Unit` and `Operating Margin` as numeric values.
- Verified consistency in brand and retailer naming (e.g., Coca-Cola, Target, Walmart).
- Removed duplicates and incomplete entries with null values for sales or profit.

---

## Data Processing  
The dataset was processed using **Power BI** with:
- DAX measures to compute `Operating Margin` as `Operating Profit / Total Sales`.
- Derived KPIs: revenue vs target, quantity vs target, monthly sales trends.
- Segmentation by delivery company, retailer, region, and city.
- Color-coded map visuals and donut charts for comparative analysis.

---

## Data Analysis and Visualization  
Key visuals from the dashboard include:

- **Bar Charts** showing total sales per day and per month.
- **Pie Charts** illustrating market share by retailer.
- **Treemaps & Donuts** for regional operating profit comparison.
- **Geographic Maps** indicating volume and revenue density by U.S. states.
- **KPI Gauges** for revenue and quantity vs target metrics.
- **Tables** displaying margin, price, and unit-level detail by delivery company.

---

## Data Interpretation  
Insights gained from the dashboard:

- **Target** leads market share with over **55%** of total sales.
- **Walmart** generated the highest operating profit at **$1.6M**.
- The **South** region contributes the highest share of profit (**26%**).
- **Friday** recorded the highest daily sales ($1.4M), while **Sunday** was lowest.
- **DHL and FedEx** are top delivery partners in terms of volume and margin.
- The highest quantity sold was in **New York City (0.71M units)**.
- Margins ranged from **36% to 44%**, with average unit prices around **$0.48**.

---

## Recommendations  
Based on the analysis, we suggest:

- Strengthen operations in **high-profit regions** (e.g., South and Midwest).
- Explore expanding partnerships with **FedEx and DHL** due to consistent margins.
- Monitor **Target's dominance** to prevent over-reliance on a single retailer.
- Increase marketing in **underperforming cities** to balance geographic reach.
- Optimize pricing strategies by focusing on regions with **higher unit margins**.

---

**Thank you for reviewing this performance dashboard.**  
**For further insights, collaboration, or data access, please reach out.**

### Author  
[Serge Tahmo](https://www.linkedin.com/in/sergetahmo)
