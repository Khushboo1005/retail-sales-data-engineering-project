# Retail Sales Data Engineering Project

## Project Overview

This project demonstrates an end-to-end retail data engineering and analytics pipeline using:

- PySpark
- Databricks
- SQL
- Parquet
- Power BI

The project simulates a modern retail analytics platform by:

- ingesting raw sales data
- performing ETL and data cleaning
- building fact and dimension tables
- implementing a star schema
- generating business KPIs
- creating an interactive Power BI dashboard

---

## Architecture

```text
Raw CSV Data
      ↓
Bronze Layer (Raw Ingestion)
      ↓
Silver Layer (Data Cleaning & Standardization)
      ↓
Gold Layer (Fact & Dimension Tables)
      ↓
Parquet Files
      ↓
Power BI Dashboard & KPIs
```

---

## Technologies Used

- PySpark
- Databricks Community Edition
- Power BI
- SQL
- Python
- Parquet
- Star Schema Modeling
- Dimensional Modeling

---

## Project Workflow

### Bronze Layer
- Raw CSV ingestion
- Schema validation

### Silver Layer
- Data cleaning
- Date standardization
- Checking duplicates
- Null handling

### Gold Layer
- Fact table creation
- Dimension table creation
- KPI generation

---

## Power BI Dashboard

### Features
- Monthly Revenue Trend
- Revenue by Category
- Revenue by Region
- KPI Cards
- Interactive slicers

---

## Business KPIs

- Total Revenue
- Total Profit
- Profit Margin
- Total Orders

---

## Repository Structure

```text
retail-sales-data-engineering-project/
│
├── notebooks/
├── architecture/
├── dashboard/
└── README.md
```

---

## Dashboard Preview

<img width="1017" height="535" alt="image" src="https://github.com/user-attachments/assets/4f270fa5-71f5-4ec9-b032-e128046dac2a" />

---

## Author

Khushboo Chandrakar
