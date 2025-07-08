# Project: Analyze the Global Cyber Attack Dashboard (2015–2024)

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

🌀 *What if the internet had dreams? Would it dream of dancing firewalls, swirling data packets, or a VPN on a unicorn? Or would it have nightmares of ransomware, brute-force attacks, and suspicious logins from "unknown"? Somewhere in cyberspace, your 2013 Tumblr password is still floating around—and someone, somewhere, just tried to use it.*

This project explores **global cyber attack trends** from 2015 to 2024 using an interactive Power BI dashboard. The dataset captures critical dimensions such as attack type, source, financial loss, affected users, and the speed of resolution. The goal is to uncover patterns in digital threats, vulnerabilities, and defense strategies to better inform security postures and incident response planning.

The analysis aims to answer:
- Which countries experienced the most significant cyber attacks?
- What attack types were most common and most costly?
- Which industries were the most frequently targeted?
- What are the top vulnerability types exploited?
- How effective were defense mechanisms over time?
- What’s the average resolution time per incident?

---

## Data Acquisition and Preparation  

The dataset includes the following 10 fields:

- `Country`
- `Year`
- `Attack Type`
- `Target Industry`
- `Financial Loss (in Million $)`
- `Number of Affected Users`
- `Attack Source`
- `Security Vulnerability Type`
- `Defense Mechanism Used`
- `Incident Resolution Time (in Hours)`

Each row represents a reported cyber incident within the given year and region, including both technical and business-level impact metrics.

---

## Data Cleaning  

The data cleaning process involved:

- Removing duplicate incident records based on `Country`, `Year`, `Attack Type`, and `Target Industry`
- Replacing nulls in critical fields like `Financial Loss` and `Number of Affected Users` with interpolated or average values
- Standardizing values for `Attack Type`, `Target Industry`, and `Security Vulnerability Type` for consistency (e.g., “SQL Injection” vs “Sql injection”)
- Filtering out entries with resolution time of zero or invalid negative values
- Normalizing country and industry labels for visual clarity

---

## Data Processing  

All transformation and modeling was performed in **Power BI**, including:

- Calculating total and average financial loss per attack and per country
- Deriving `Attack Frequency` and `Average Resolution Time` per year
- Grouping incidents by vulnerability type and mapping defense strategies
- Categorizing attacks by `Source` (Insider, Nation-State, Hacktivist, Unknown)
- Extracting trends across time to observe year-over-year changes

---

## Data Analysis and Visualization  

The interactive Power BI dashboard features:

- **KPI Cards** for:
  - Total Financial Loss
  - Total Affected Users
  - Top Attack Type
  - Country with Highest Incident Count
- **Bar Charts** for:
  - Attacks by Country
  - Industry-wise Attack Distribution
  - Attack Source Frequency
- **Donut Charts** comparing:
  - Security Vulnerability Types
  - Defense Mechanisms Used
- **Line Charts** for:
  - Yearly trends in Financial Loss and Affected Users
- **Scatter Plot** showing correlation between Financial Loss and Incident Resolution Time
- **Slicers** to filter by Year, Country, Attack Type, and Industry

---

## Data Interpretation  

Key insights from the analysis include:

- The **Finance, Government, and Healthcare** industries faced the most frequent and severe attacks
- **Phishing, Ransomware**, and **DDoS** were the most common and high-cost attack types
- The **United States, UK, and Germany** recorded the highest financial losses over the period
- **Insider threats** accounted for over **25%** of reported attacks, followed by **Nation-State actors**
- **Encryption and Firewalls** were the most commonly deployed defense mechanisms
- Average incident resolution time ranged between **12–72 hours**, with certain industries lagging in response

---

## Recommendations  

Based on the insights:

- Invest in proactive defense measures such as **AI-based threat detection**, especially in high-risk industries
- Strengthen access control systems to combat **insider threats**
- Increase global cooperation in monitoring and responding to **nation-state sponsored attacks**
- Mandate regular **security audits and patching cycles** for critical systems
- Use attack resolution benchmarks to optimize **incident response teams** and SLAs

---

**Thank you for reviewing this cyber threat analysis.**  
To explore the live dashboard, please access the link below:

🔗 [View Cyber Attack Power BI Dashboard](https://app.powerbi.com/groups/your-dashboard-link)

---

### Author  
[Your Name](https://github.com/yourgithub)
