# 💊 Pharma Data Lakehouse ETL/ELT in Azure Synapse

This project implements an automated ETL/ELT pipeline in Azure Synapse Analytics for a pharmaceutical company operating in the EU. It standardizes data processing across multiple sources: ERP system, distributors, and pharmacy market sales.

## 🧱 Lakehouse Architecture (Medallion)

The data pipeline is structured into three layers following the Medallion architecture pattern:

🟤 Bronze Layer – Raw Ingestion
Raw data is ingested without transformation.

Sources: ERP (MySQL), distributors (MinIO), and CSV exports from pharmacy data providers.

Stored in Delta Lake format on Azure Data Lake Gen2.

⚪ Silver Layer – Cleaned and Standardized
Data is validated, deduplicated, typecasted, and joined into consistent structures.

Business rules and quality checks are applied.

Output: reliable, unified, and queryable Delta tables.

🟡 Gold Layer – Analytical Model
Analytical star-schema model for reporting (fact and dimension tables).

Pre-aggregated KPIs: e.g., sales volume, value, market share.

Ready for reporting in Power BI.


## 🎯 Objectives

- Eliminate manual data preparation and mapping errors
- Unify data formats across countries and sales channels
- Automate monthly demand and operations planning input
- Enable Power BI dashboards and future AI integrations

## ⚙️ Technologies

- Azure Synapse Analytics (Serverless SQL, Spark, Pipelines)
- Delta Lake on ADLS Gen2
- Python, SQL
- Power BI
- Azure Key Vault

## 📊 Outcome

- ~30 minutes end-to-end data preparation (vs. days manually)
- Reliable, standardized data across all EU regions
- Model ready for executive and operational analytics
- Foundation for machine learning–driven forecasting

## 📁 Structure

- `/minio`: CSV files
- `/MySql`: sample database
- `/PowerBi`: Dashboards and visuals
- `/SynapseAnalytics`: ETL/ELT

## 📜 License

MIT – free to use, modify and distribute.
