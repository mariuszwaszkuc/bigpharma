# 💊 Pharma Data Lakehouse ETL/ELT in Azure Synapse

This project implements an automated ETL/ELT pipeline in Azure Synapse Analytics for a pharmaceutical company operating in the EU. It standardizes data processing across multiple sources: ERP system, distributors, and pharmacy market sales.

## 🧱 Architecture

The pipeline follows the Lakehouse architecture using the Medallion structure:

- **Bronze layer**: Raw data ingestion (MySQL, MinIO, CSV)
- **Silver layer**: Data cleaning, deduplication, validation
- **Gold layer**: Analytical star-schema model for reporting

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
