# Project: Analyze the Employee Leadership Dashboard

## Table of Contents  
1. [Introduction](#introduction)  
2. [Data Acquisition and Preparation](#data-acquisition-and-preparation)  
3. [Data Cleaning](#data-cleaning)  
4. [Data Processing](#data-processing)  
5. [Data Analysis and Visualization](#data-analysis-and-visualization)  
6. [Data Interpretation](#data-interpretation)  
7. [Recommendations](#recommendations)  

## Introduction  
This project focuses on the development and analysis of an **Employee Leadership Dashboard**. The dashboard provides insights into workforce demographics, leadership roles, educational backgrounds, industry distribution, and career progression across 5 countries and 5 U.S. states.

The analysis seeks to answer the following key questions:
- What is the distribution of leadership roles across industries and countries?
- How many employees have been promoted or transferred, and what were the reasons?
- How do age and experience correlate with leadership roles?
- What is the gender and education breakdown of leadership employees?
- How have employee counts evolved over the years?

## Data Acquisition and Preparation  
The employee dataset consists of the following 16 columns:

`Employee ID`, `Employee Name`, `Leadership Role`, `Industry`, `Start Date`, `End Date`, `Gender`, `Age`, `Years in Role`, `Years of Experience`, `Previous Role`, `New Role`, `Reason for Promotion/Transfer`, `Country`, `State`, `Degree`

This data captures both historical and current information on 5,000 employees across multiple roles and locations.

## Data Cleaning  
The following cleaning steps were taken:
- Removed duplicate `Employee ID` entries.
- Standardized date fields (`Start Date`, `End Date`) into a consistent date format.
- Normalized categorical values such as `Leadership Role`, `Degree`, `Gender`, and `Country`.
- Addressed null values in `Previous Role`, `New Role`, and `Reason for Promotion/Transfer` with contextual imputations or exclusions.
- Converted experience fields (`Years in Role`, `Years of Experience`) into numeric format for aggregation and comparison.

## Data Processing  
Using **Power BI**, the dataset was transformed through Power Query, including:
- Deriving new columns such as `Tenure` (End Date – Start Date) and `Promotion Year`.
- Creating relationships between fields for slicing and drill-down.
- Grouping leadership data by region, state, and country.
- Assigning bins for Age (e.g., 20–30, 31–40) and Years of Experience for trend visualizations.

## Data Analysis and Visualization  
Key visualizations from the dashboard include:

- **Donut Charts** for degree distribution and employee location by country.  
- **Bar Charts** showing the number of employees per role and per country.  
- **Treemap** displaying experience per leadership role.  
- **Line Chart** tracking employee count trends from 2015 to 2023.  
- **Map Visualization** of employee experience by U.S. state.  
- **Filter Panel** allowing user-defined selections based on gender, country, industry, leadership role, and year range.

These visuals enable dynamic analysis of workforce characteristics and leadership trends.

## Data Interpretation  
From the dashboard, we gained several key insights:
- The organization employs **5,000 individuals**, equally split between **male and female**.
- **Bachelor’s and Master’s degrees** dominate the workforce’s educational profile, each with over 1.2K employees.
- The **Manager** and **Director** roles show the highest leadership experience with over **17K years** combined.
- The USA and Germany represent the highest employee counts, each with over 1,000 employees across various industries.
- **Performance-based promotions** and **business needs** are the leading reasons for role changes.
- Employee count peaked in **2021** at 659 and declined to **270** in 2023, signaling a possible workforce reduction or restructuring trend.

## Recommendations  
Based on the insights from the dashboard, the following actions are suggested:
- Focus on strengthening leadership pipelines in **C-Level and VP roles** to balance experience distribution.
- Investigate the **2023 employee drop** to determine causes and take retention-focused actions.
- Increase efforts to support **educational development**—employees with advanced degrees may influence leadership strength.
- Review promotion and transfer processes to ensure consistency and alignment with performance goals.

<br/>

**Thank you for taking the time to review this report!**  
**For updates, collaboration, or dashboard access, please reach out.**

### Author  
[Serge Tahmo](https://github.com/Sergetahmo)

