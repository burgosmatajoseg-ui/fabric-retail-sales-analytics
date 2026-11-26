# 🚀 Retail Sales Analytics Platform using Microsoft Fabric

## Overview

This project demonstrates the design and implementation of a modern Retail Analytics Platform using Microsoft Fabric and Lakehouse architecture principles.

The solution centralizes retail sales data from multiple sources, applies data transformation and quality processes, and provides analytics-ready datasets for reporting and decision-making.

The objective is to showcase practical knowledge in:

- Microsoft Fabric
- Data Factory
- OneLake
- Lakehouse Architecture
- Data Engineering
- SQL Analytics
- ETL / ELT
- Power BI
- Data Modeling

---

# Business Scenario

A retail organization receives operational data from various business systems including:

- Point of Sale (POS)
- Inventory Management
- ERP
- E-Commerce Platform
- Loyalty Program

The organization requires a centralized platform capable of:

- Integrating data from multiple sources
- Storing data in a unified architecture
- Performing transformations and validations
- Producing business KPIs
- Supporting reporting and analytics

---

# Solution Architecture

architecture/lakehouse_architecture.png

# Technologies Used

| Technology | Purpose |
|------------|----------|
| Microsoft Fabric | Data Platform |
| Fabric Data Factory | Data Ingestion |
| OneLake | Central Storage |
| Lakehouse | Data Architecture |
| PySpark | Data Transformation |
| SQL Endpoint | Data Querying |
| Power BI | Analytics & Reporting |

---

# Data Architecture

## Bronze Layer

Raw ingestion area.

Characteristics:

- Original source data
- Minimal transformations
- Historical storage
- Auditability

Examples:

```text
bronze_sales
bronze_customers
bronze_products
```

---

## Silver Layer

Data cleansing and standardization.

Processes:

- Data Quality Validation
- Null Handling
- Data Standardization
- Duplicate Removal

Examples:

```text
silver_sales
silver_customers
silver_products
```

---

## Gold Layer

Business-ready datasets.

Examples:

```text
gold_sales_summary
gold_customer_metrics
gold_product_performance
```

Used directly by reporting and analytics solutions.

---

# ETL / ELT Process

## Step 1 - Data Ingestion

Source files are loaded through Fabric Data Factory pipelines into OneLake.

Sources include:

- CSV
- SQL Server
- Oracle
- REST APIs

---

## Step 2 - Data Transformation

Transformations are executed through notebooks and SQL processes.

Examples:

- Data Cleansing
- Standardization
- Business Rule Validation
- KPI Calculation

---

## Step 3 - Data Serving

Curated datasets are exposed through:

- Lakehouse SQL Endpoint
- Semantic Models
- Power BI Reports

---

# Repository Structure

```text
fabric-retail-sales-analytics
│
├── README.md
│
├── architecture
│   ├── lakehouse_architecture.png
│   ├── data_flow.png
│   └── bronze_silver_gold.png
│
├── sql
│   ├── create_dimensions.sql
│   ├── create_fact_sales.sql
│   ├── sales_kpis.sql
│   └── top_products.sql
│
├── screenshots
│   ├── workspace.png
│   ├── data_pipeline.png
│   ├── lakehouse.png
│   ├── notebook.png
│   └── powerbi_dashboard.png
│
└── notebooks
    └── sales_transformations.py
```

---

# Example Business KPIs

The platform generates key retail metrics such as:

- Total Sales
- Sales by Store
- Sales by Product Category
- Top Customers
- Average Ticket
- Monthly Revenue Trend
- Product Performance
- Customer Retention

---

# Sample SQL Query

```sql
SELECT
    YEAR(sale_date) AS year,
    MONTH(sale_date) AS month,
    SUM(amount) AS total_sales
FROM fact_sales
GROUP BY
    YEAR(sale_date),
    MONTH(sale_date)
ORDER BY
    year,
    month;
```

---

# Power BI Dashboard

Example dashboard components:

### Executive Overview

- Revenue
- Transactions
- Customers

### Product Analytics

- Top Products
- Category Performance

### Store Analytics

- Sales by Store
- Regional Performance

### Customer Insights

- Customer Segmentation
- Purchase Behavior

---

# Data Engineering Concepts Demonstrated

This project demonstrates:

✅ Data Ingestion

✅ ETL / ELT

✅ Lakehouse Architecture

✅ Medallion Architecture

✅ Data Quality

✅ OneLake

✅ Fabric Data Factory

✅ SQL Analytics

✅ Data Modeling

✅ Power BI Integration

✅ Data Governance Principles

✅ PySpark Transformations

---

# Future Enhancements

Planned improvements include:

- Incremental Loads
- CDC (Change Data Capture)
- Real-Time Analytics
- Data Quality Framework
- CI/CD Deployment
- Automated Monitoring
- Data Lineage

---

# Author

José Guadalupe Burgos Mata

Senior ETL Developer | Data Engineer

Specialist in Enterprise Data Integration, ETL Development, Data Warehousing, Microsoft Fabric and Modern Data Platforms.

Website:
https://joseburgos-dataengineer.com


---
