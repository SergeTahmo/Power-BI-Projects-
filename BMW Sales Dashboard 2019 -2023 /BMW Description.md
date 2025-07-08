# Project: Analyze the BMW Sales Performance Dashboard (2019–2023)

## Table of Contents  
1. [Introduction](#introduction)  
2. [Data Acquisition and Preparation](#data-acquisition-and-preparation)  
3. [Data Cleaning](#data-cleaning)  
4. [Data Processing](#data-processing)  
5. [Data Analysis and Visualization](#data-analysis-and-visualization)  
6. [Data Interpretation](#data-interpretation)  
7. [Recommendations](#recommendations)  

## Introduction  
This project analyzes **BMW vehicle sales performance** from 2019 to 2023. The dataset includes information on sales quantity, revenue, regional breakdowns, sales channels, and model performance across multiple countries.  

The analysis aims to address the following:
- Which BMW models generated the highest revenue?
- How did sales evolve year-over-year between 2019 and 2023?
- Which regions and countries contributed most to sales?
- What was the performance of online vs in-person (offline) channels?
- How did model popularity differ by region?

## Data Acquisition and Preparation  
The dataset consists of the following 10 columns:

`Date`, `Year`, `Model`, `Revenue`, `Quantity Sold`, `Region`, `Country`, `Channel`, `Car URL`, `Flag URL`

These fields represent transactional sales data, grouped by geography, sales medium, and car model.

## Data Cleaning  
The following cleaning steps were implemented:
- Converted the `Date` field into a standardized date format.
- Verified numerical consistency in `Revenue` and `Quantity Sold` by removing formatting symbols and casting them to numeric types.
- Removed or imputed missing data for `Model`, `Country`, or `Channel`.
- Standardized `Region`, `Channel`, and `Country` values for consistency (e.g., “Online” vs “online”).
- Verified that all `Car URL` and `Flag URL` links are valid or excluded broken ones.

## Data Processing  
Data transformation was performed in **Power BI**, including:
- Extracting `Month` and `Quarter` from the `Date` field for time series analysis.
- Aggregating revenue and sales by `Model`, `Region`, and `Channel`.
- Creating KPI cards for total revenue, total cars sold, top model, and top region.
- Setting up relationships to allow drill-down by year, model, and geography.
- Enabling clickable thumbnails using `Car URL` and flag icons with `Flag URL`.

## Data Analysis and Visualization  
The Power BI dashboard includes the following visuals:
- **Line Chart** for revenue trends from 2019–2023.
- **Stacked Bar Chart** showing quantity sold by region and year.
- **Donut Chart** for model distribution based on revenue.
- **Table with Car & Flag Images** using `Car URL` and `Flag URL`.
- **Card KPIs** for:
  - Total Revenue
  - Total Units Sold
  - Top-Selling Model
  - Best-Performing Country
- **Map Visualization** for geographic performance.
- **Slicers/Filters** by Year, Country, Channel, and Model.

## Data Interpretation  
Insights derived from the analysis include:
- The highest revenue year was **2021**, showing a recovery after a dip in 2020 (COVID-19 impact).
- The **BMW X5** and **3 Series** were consistently top performers in revenue and quantity sold.
- **Europe and North America** were the strongest regions, contributing over 60% of total revenue.
- **Online channels** saw steady growth year over year, especially during 2020–2022.
- Germany, USA, and China were the top 3 countries in terms of total revenue.

## Recommendations  
Based on the trends observed:
- Expand inventory and marketing efforts for top models like **X5** and **3 Series**.
- Invest further in **online sales channels**, which continue to show strong adoption.
- Consider region-specific strategies: e.g., launch new models first in high-performing countries.
- Analyze countries with low performance and evaluate if issues are related to pricing, availability, or demand.

<br/>

**Thank you for reviewing this report.**  
To explore the live dashboard, please access the link below:

🔗 [View BMW Power BI Dashboard](https://app.powerbi.com/groups/your-dashboard-link)

---

### Author  
[Serge Tahmo](https://github.com/Sergetahmo)
