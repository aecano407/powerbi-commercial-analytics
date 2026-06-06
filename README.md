# 📊 Power BI — Commercial Analytics Dashboards

> **Business Intelligence solutions for commercial analytics, sales performance, and executive decision-making.**

[![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)]()
[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)]()
[![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)]()

---

## 🎯 Overview

This repository contains a collection of **Power BI dashboards and analytical models** developed for commercial analytics use cases in retail, pharma, and BPO environments.

The focus areas include:
- Sales performance tracking and trend analysis
- KPI monitoring for commercial and operational areas
- Distribution channel behavior and customer segmentation
- Workforce analytics and operational efficiency reporting
- Executive-level reporting for strategic decision-making

---

## 🗂️ Repository Structure

```
powerbi-commercial-analytics/
│
├── 📁 dashboards/          # Power BI .pbix files
│   ├── sales-performance/
│   ├── kpi-executive/
│   ├── channel-analytics/
│   └── workforce-analytics/
│
├── 📁 sql-queries/         # SQL queries for data extraction
│   ├── oracle/
│   └── sql-server/
│
├── 📁 dax-measures/        # DAX measures and calculated columns library
│
├── 📁 power-query/         # Power Query M transformation scripts
│
└── 📁 docs/               # Documentation and screenshots
```

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and visualization |
| **DAX** | Calculated measures, KPIs, time intelligence |
| **Power Query (M)** | Data transformation and ETL |
| **Oracle Database** | Primary data source (PL/SQL queries) |
| **SQL Server** | Secondary data source (T-SQL) |
| **Excel** | Data validation and ad-hoc analysis |
| **Python (Pandas)** | Data preprocessing scripts |

---

## 📈 Key Dashboard Categories

### 1. 🏪 Sales Performance Dashboard
- Revenue tracking vs. budget by region, product, and channel
- Month-over-month and year-over-year comparison
- Top/bottom performers by sales representative
- Trend forecasting using linear regression in DAX

### 2. 📌 Executive KPI Dashboard
- C-level summary view with critical business metrics
- Real-time data refresh via scheduled gateway
- Traffic light indicators for performance thresholds
- Drill-through to operational detail

### 3. 🚚 Distribution Channel Analytics
- Channel performance comparison (direct, distributor, retail)
- Geographic heat maps for territory coverage
- Customer behavior segmentation and frequency analysis
- Product portfolio mix by channel

### 4. 👥 Workforce Analytics (BPO)
- Agent productivity and adherence tracking
- Absenteeism trend analysis
- Headcount vs. capacity planning
- SLA and operational KPI monitoring

---

## 🔧 DAX Measures Library

```dax
-- YTD Sales
YTD Sales = TOTALYTD([Total Sales], Calendar[Date])

-- Sales Growth %
Sales Growth % = 
DIVIDE(
    [Total Sales] - [Total Sales LY],
    [Total Sales LY],
    0
)

-- Running Total
Running Total = 
CALCULATE(
    [Total Sales],
    FILTER(
        ALLSELECTED(Calendar[Date]),
        Calendar[Date] <= MAX(Calendar[Date])
    )
)
```

---

## 📋 Requirements

- Power BI Desktop (latest version)
- SQL Server / Oracle Database connection (or sample data files)
- Power BI Gateway for scheduled refresh (optional)

---

## 👤 Author

**Americo Enrique Cano Sibrian**  
Business Intelligence & Analytics Specialist | Guatemala

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/americo-cano-bi/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aecano407@gmail.com)

---

*Part of the BI & Data Analytics portfolio — transforming data into competitive advantages.*
