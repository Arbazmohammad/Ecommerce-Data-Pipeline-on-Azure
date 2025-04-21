# Azure Data Engineering Project – E-commerce Analytics Pipeline
🚀 Overview
This project demonstrates a full-scale end-to-end cloud data pipeline for processing and analyzing E-commerce data using Microsoft Azure services. The primary goal was to ingest raw data from external APIs, transform and model it using industry-standard tools, and finally visualize insights with Power BI for business analysis.

## Architechture Diagram
<img width="1459" alt="Architecture Diagram" src="https://github.com/user-attachments/assets/b501f776-928b-4546-b574-3c60e4332930" />

## 🏗️ Architecture & Tools Used
🔹 Ingestion Layer (Bronze)
Azure Data Factory: Designed dynamic Copy Activity pipelines to fetch multiple data files from REST APIs.

Azure Data Lake Storage (Gen2): Used as a data lake with a layered structure (Bronze/Silver/Gold).

<img width="468" alt="image" src="https://github.com/user-attachments/assets/76e461a8-2415-47ce-910a-b94906b58e9f" />


Ingested raw JSON/CSV files directly into the Bronze layer for initial storage.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/a03f305b-00d2-4185-80b2-33f6abbe6dfc" />

🔹 Transformation Layer (Silver)
Azure Databricks: Processed and cleaned the raw data using PySpark, performing:

Schema normalization

Null handling and filtering

Data enrichment and joins

Transformed data stored as Parquet files in the Silver layer for optimal querying.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/227c2f78-29c2-4845-a540-b8ac72b05277" />


🔹 Modeling & Serving Layer (Gold)
Azure Synapse Analytics:

Created external tables and views on top of Parquet files.

Utilized T-SQL to build analytics-ready data models and perform aggregations.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/1dd01eb9-11ee-4189-b815-3b1cf62efc87" />


🔹 Visualization
Power BI: Connected directly to Synapse external tables and developed interactive dashboards for:

Sales trends

<img width="434" alt="image" src="https://github.com/user-attachments/assets/672ea22c-e5f1-4f04-ad23-1c8aec35bbc2" />


Customer segmentation

Product performance

## 🧠 Key Learnings & Highlights
Hands-on experience with cloud-native ETL on Azure.

Effective use of layered architecture (Bronze, Silver, Gold) to manage data transformation stages.

Integration of ADF, ADLS, Databricks, Synapse, Power BI into a unified workflow.

Gained expertise in querying large datasets using SQL in Synapse.

Overcame real-world issues like API throttling, schema mismatches, and optimizing joins for performance.

## 📊 Project Folder Structure
graphql
Copy
Edit
├── notebooks/
│   └── transformation_jobs.ipynb    # PySpark notebooks in Databricks
├── pipelines/
│   └── adf_pipeline.json            # ADF pipeline definitions (ARM templates)
├── sql/
│   └── synapse_views.sql            # SQL scripts for Synapse Analytics
├── dashboards/
│   └── powerbi_report.pbix          # Power BI dashboards
├── README.md

## 💻 Technologies Used
Azure Data Factory

Azure Data Lake Storage Gen2

Azure Databricks (PySpark)

Azure Synapse Analytics (SQL)

Power BI

Azure IAM & Security

## 📌 Use Cases
E-commerce sales analysis

Customer purchase behavior

Product trend insights

Revenue performance by region/category

## ✅ Future Enhancements
Automate pipeline with ADF triggers and parameterization

Add CI/CD using Azure DevOps

Enable alerting for data quality using Great Expectations

Feel free to fork, explore, or contribute!

🔗 Let’s connect on LinkedIn if you’d like to chat more about cloud data engineering!
