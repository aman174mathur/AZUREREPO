# End-to-End Azure Data Engineering Pipeline

## Project Overview
This project demonstrates a complete **end-to-end data engineering pipeline on Microsoft Azure**.  
The pipeline extracts data from a MySQL database, processes it using Azure Databricks, stores it in Azure Synapse Analytics, and visualizes insights using Power BI.

## Architecture

MySQL → Azure Data Factory → Azure Blob Storage → Azure Databricks → Azure Synapse Analytics → Power BI

![Architecture](architecture/architecture-diagram.png)

## Tech Stack

- Azure Data Factory
- Self Hosted Integration Runtime
- Azure Blob Storage
- Azure Databricks (PySpark)
- Azure Synapse Analytics
- Power BI
- MySQL

## Pipeline Workflow

### 1 Data Extraction
Azure Data Factory copies data from the MySQL Employees database into Azure Blob Storage.

Key Activities:
- Lookup Activity
- ForEach Loop
- Copy Data Activity

### 2 Data Transformation
Azure Databricks processes raw files using PySpark.

Transformations include:
- Data cleaning
- Standardizing column names
- Removing null values
- Writing output in Delta/Parquet format

### 3 Pipeline Automation
ADF orchestrates Databricks notebooks for automated processing of all tables.

### 4 Data Loading
Processed data is loaded into Azure Synapse Analytics for analytical querying.

### 5 Data Visualization
Power BI dashboards provide insights into:

- Employee demographics
- Department distribution
- Salary analysis

## Key Features

- Fully automated ETL pipeline
- Scalable architecture
- Distributed data processing with Spark
- Analytical data warehouse using Synapse
- Business intelligence dashboard with Power BI

## Example Dashboard

![Dashboard](images/powerbi_dashboard.png)

## Future Improvements

- Add incremental data loading
- Implement data quality checks
- Add CI/CD using Azure DevOps
