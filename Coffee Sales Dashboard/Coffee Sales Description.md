# Project: Analyze the Coffee Sales Performance Dashboard (2022–2023)

## Table of Contents  
1. [Introduction](#introduction)  
2. [Data Acquisition and Preparation](#data-acquisition-and-preparation)  
3. [Data Cleaning](#data-cleaning)  
4. [Data Processing](#data-processing)  
5. [Data Analysis and Visualization](#data-analysis-and-visualization)  
6. [Data Interpretation](#data-interpretation)  
7. [Recommendations](#recommendations)  

## Introduction  
This project explores **coffee sales performance** across multiple store locations from 2022 to 2023. The dataset contains individual transaction records, store-level details, and product specifications. The objective is to uncover patterns in sales quantity, unit pricing, store trends, and time-based behaviors to support better inventory and promotional decisions.

The analysis aims to answer:
- What product categories and types are the most sold?
- Which store locations generated the highest revenue?
- How do sales vary across time (hour, day, month)?
- What is the average revenue per transaction?
- Which time slots or weekdays drive the most transactions?

## Data Acquisition and Preparation  
The dataset includes the following 11 fields:

`transaction_id`, `transaction_date`, `transaction_time`, `transaction_qty`, `store_id`, `store_location`, `product_id`, `unit_price`, `product_category`, `product_type`, `product_detail`

Each row represents a point-of-sale coffee transaction and includes store-level and product-level attributes.

## Data Cleaning  
The data cleaning process included:
- Removing duplicate transactions based on `transaction_id`, `transaction_date`, and `store_id`.
- Converting `transaction_date` to a proper date format and `transaction_time` to time (24-hour).
- Replacing negative or zero values in `transaction_qty` or `unit_price` with median or default values.
- Normalizing values for `store_location`, `product_category`, and `product_type` to consistent casing and spacing.
- Checking for nulls in key fields and filling or excluding incomplete rows as needed.

## Data Processing  
All processing and modeling were performed in **Power BI**, where:
- `Month`, `Weekday`, and `Hour` were extracted from `transaction_date` and `transaction_time`.
- `Total Revenue` was calculated as `transaction_qty × unit_price`.
- Products were grouped by category and type to determine best-sellers.
- Sales trends were aggregated by `store_location`, `time of day`, and `product_type`.

## Data Analysis and Visualization  
The interactive Power BI dashboard features:
- **KPI Cards** for:
  - Total Revenue
  - Total Transactions
  - Top-Selling Product Type
  - Store with Highest Sales
- **Line Chart** showing daily/weekly revenue trends.
- **Donut Chart** comparing product category contributions.
- **Bar Charts** for:
  - Sales by store location
  - Quantity sold by hour of day
  - Revenue by product type
- **Slicers** to filter by date, store, product category, and product type.

## Data Interpretation  
Key findings from the analysis include:
- **Espresso** and **Cappuccino** were the most frequently sold product types.
- The highest sales occurred between **8 AM and 11 AM**, aligning with morning traffic.
- **Store #102 (Downtown Location)** recorded the highest total revenue.
- Sales volume spiked during weekends, especially **Saturday mornings**.
- The average revenue per transaction was **$6.28**, with variation by store and category.

## Recommendations  
Based on the insights:
- Increase inventory of high-performing products like **Espresso** and **Cappuccino**, especially during peak hours.
- Focus staffing and promotional offers between **8 AM and 11 AM**, particularly on weekends.
- Replicate strategies used in high-performing stores (e.g., Store #102) across other branches.
- Explore bundling options or loyalty discounts to raise average transaction revenue.

<br/>

**Thank you for reviewing this report.**  
To explore the live dashboard, please access the link below:

🔗 [View Coffee Sales Power BI Dashboard](https://app.powerbi.com/groups/your-dashboard-link)

---

### Author  
[Serge Tahmo](https://github.com/Sergetahmo)
