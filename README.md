# SQL Data Warehouse Project

A SQL Server-based data warehouse project that integrates CRM and ERP data using a Medallion Architecture (Bronze, Silver, Gold) and prepares data for analytical reporting.

## Project Overview

This project demonstrates the development of a data warehouse using SQL Server and T-SQL. Raw data from CRM and ERP sources is processed through different data layers and transformed into business-ready data for analytics.

The project focuses on:

- Data integration
- ETL processes
- Data transformation
- Data modeling
- Data quality validation
- Analytical data preparation

## Architecture

The project follows the Medallion Architecture:

### Bronze Layer
Stores raw data from the source systems in its original form.

### Silver Layer
Processes and transforms the raw data through standardization, normalization, and integration.

### Gold Layer
Provides business-ready data using fact and dimension tables designed for analytical reporting.

## Data Flow

Source Systems
→ Bronze Layer
→ Silver Layer
→ Gold Layer
→ Analytics

The source data consists of CRM and ERP datasets that are integrated and transformed through the warehouse layers.

## Data Model

The Gold layer follows a Star Schema consisting of:

### Dimension Tables

- `gold.dim_customers`
- `gold.dim_products`

### Fact Table

- `gold.fact_sales`

The fact table connects to the customer and product dimensions using surrogate keys.

## ETL Process

The ETL workflow includes:

1. Loading raw source data into the Bronze layer.
2. Transforming and standardizing data in the Silver layer.
3. Integrating the processed data into business entities.
4. Loading analytical structures into the Gold layer.
5. Performing data quality and integration checks.

## Data Quality

The project includes validation checks for:

- Data completeness
- Schema consistency
- Data correctness
- Data integration
- Relationships between fact and dimension tables

## Technologies

- SQL Server
- T-SQL
- ETL
- Data Warehousing
- Data Integration
- Data Modeling

## Repository Structure

```text
sql-data-warehouse/
│
├── dataset/
│   ├── source_crm/
│   └── source_erp/
|
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── docs/
│   └── naming_conventions.md
│
├── tests/
│   ├── quality_checks_gold.sql
│   └── quality_checks_silver.sql
│
└── README.md
```

## Acknowledgments

This project was developed as part of my learning journey in SQL Data Warehousing, based on the **SQL Data Warehouse Project by Data With Baraa**. The project helped me understand practical concepts including ETL, Medallion Architecture, data integration, data modeling, and data quality validation.

Special thanks to [Baraa Khatib Salkini](https://www.linkedin.com/in/baraa-khatib-salkini) for the educational resources and project guidance.
