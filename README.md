# retail-sales-data-engineering-project

**Project Overview**

      This project demonstrates an end-to-end retail data engineering and analytics pipeline using PySpark, Databricks,     Parquet, dimensional modeling, and Power BI.
      
      The goal of the project is to simulate a modern retail analytics platform by:
      
      ingesting raw sales data
      performing ETL and data cleaning
      building fact and dimension tables
      implementing a star schema
      generating business KPIs
      creating an interactive Power BI dashboard
      
      The project follows a simplified medallion/lakehouse architecture using Bronze, Silver, and Gold layers.

**Architecture**
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

**Technologies Used**
    PySpark
    Databricks Community Edition
    Power BI
    Parquet
    SQL
    Python
    Star Schema Modeling
    Dimensional Modeling

**Data Pipeline**
    **Bronze Layer**
      Raw retail CSV data ingested into Databricks without modification.    
    **Tasks Performed**
      CSV ingestion
      Schema inspection
      Raw data validation

  **Silver Layer**
    Data cleaning and transformation layer.
  **Transformations**
    Standardized column names
    Handled inconsistent date formats
    Converted string columns to numeric datatypes
    Removed malformed numeric separators
    Performed null and duplicate checks
    Applied schema enforcement
  **Data Quality Challenges**
    Mixed date formats (M/d/yyyy and dd-MM-yyyy)
    Numeric columns containing commas
    Duplicate/non-unique product IDs

  **Gold Layer**
    Business-ready warehouse layer.
    **Fact Table**
      fact_sales:      
        sales
        profit
        quantity
        shipping_cost
        order_priority
        
  **Dimension Tables**
    dim_customer:
        customer_id
        customer_name
        segment
        market
        region
        country
        state
        
    dim_product:
        product_key
        product_name
        category
        sub_category
        
    dim_region:
        region_key
        market
        region
        country
        state

**Data Modeling**
    The project uses a Star Schema design.    
      **Features**
          Fact & Dimension modeling
          Surrogate key generation
          Relationship modeling in Power BI
          Dimensional joins
          Business KPI calculations

**Power BI Dashboard**
    Dashboard Features:
        Monthly Revenue Trend
        Revenue by Category
        Revenue by Region
        KPI Cards
        Total Revenue
        Total Profit
        Total Orders
        Profit Margin
        Interactive slicers
        YearMonth
        Category
        Region

**Business KPIs**
    Examples of KPIs generated:    
        Total Revenue
        Profit Margin
        Regional Sales Performance
        Category-wise Revenue
        Monthly Revenue Trends
        Top Customers
    
**Sample PySpark Transformations**
    **Date Standardization**
      coalesce(
          expr("try_to_timestamp(order_date, 'M/d/yyyy')"),
          expr("try_to_timestamp(order_date, 'dd-MM-yyyy')")
      )
    **Numeric Standardization**
      regexp_replace(col("sales"), ",", "").cast("double")
    **Surrogate Key Generation**
      monotonically_increasing_id()

**Project Structure**
    retail-sales-data-engineering-project/
    │
    ├── notebooks/
    ├── architecture/
    ├── screenshots/
    ├── dashboard/
    ├── README.md
    └── data_sample/

**Key Learnings**
    Building scalable ETL pipelines using PySpark
    Handling real-world data quality issues
    Implementing dimensional modeling
    Creating star schemas for analytics
    Building business dashboards in Power BI
    Working with parquet-based analytical datasets

**Future Improvements**
    Delta Lake implementation
    Incremental ETL pipelines
    Azure Data Factory integration
    dbt transformations
    Automated orchestration workflows

**Dashboard Preview**

<img width="1017" height="535" alt="image" src="https://github.com/user-attachments/assets/4f270fa5-71f5-4ec9-b032-e128046dac2a" />


**Author
Khushboo Chandrakar**
