# SalesLakehouse-Databricks

A modern Data Lakehouse project built on Databricks, implementing the Medallion Architecture (Bronze → Silver → Gold) to transform raw sales data into analytics-ready datasets.


## Project Overview

This project demonstrates an end-to-end data engineering pipeline that:

- Ingests raw sales data from multiple source systems (CRM & ERP)
- Applies progressive data quality and transformation across layers
- Builds a clean dimensional model (Star Schema) for analytics and reporting
- Leverages Databricks Lakehouse capabilities (Delta Lake, Unity Catalog / Volumes)

Goal: Turn messy transactional data into reliable, business-ready insights.


## Architecture – Medallion Layers

| Layer   | Purpose                                      | Output Tables / Views                  |
|---------|----------------------------------------------|----------------------------------------|
| Bronze | Raw data ingestion (as-is)                  | cust_info, prd_info, sales_details, CUST_AZ12, LOC_A101, PX_CAT_G1V2 |
| Silver | Data cleaning, standardization & enrichment | Cleaned Customer, Product, Sales, Category, Location tables |
| Gold   | Business-ready dimensional model            | dim_customers, dim_products, fact_sales |
