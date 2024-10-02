# Formula One Data Analysis using Azure Databricks, ADLS, ADF, and Power BI

## Overview

This project focuses on analyzing Formula One data using **Azure Databricks** and integrating various Azure services to create a robust and scalable data pipeline. Data ingestion is performed using **Azure Data Lake Storage (ADLS)**, **Azure Data Factory (ADF)** for orchestration, and **Power BI** for visualization. The project also implements best practices like **Delta Lake** for data versioning and **Unity Catalog** for managing data access.

## Key Components

### 1. Data Ingestion (ADLS)
   - Data was ingested from multiple sources such as CSV and JSON files.
   - The raw data was stored in the **ADLS Raw Layer**.

### 2. Data Transformation (Azure Databricks - PySpark / SQL)
   - **PySpark** was used for data processing, cleaning, and transformation.
   - **Spark SQL** queries were used for performing **filtering** and **joins** on datasets.
   - Data was transformed and moved to the **ADLS Ingested Layer**.
   - Implemented **incremental data load** using **Delta Lake** for efficient updates.

### 3. Data Orchestration (ADF Pipelines)
   - **Azure Data Factory** (ADF) was used to orchestrate data pipelines.
   - Pipelines were created to automate the ingestion and transformation workflows.
   - Used ADF triggers to schedule pipelines for regular execution.

### 4. Data Storage (Delta Lake & ADLS)
   - **Delta Lake** was used to enable data versioning and ensure high data quality.
   - Data was stored in the **ADLS Presentation Layer** for downstream analysis and reporting.

### 5. Data Management (Unity Catalog)
   - **Unity Catalog** was employed to provide fine-grained access control and governance for data assets.

### 6. Data Analysis and Reporting (Power BI)
   - Data was made business-ready for consumption and visualization in **Power BI**.
   - Power BI dashboards were created to display the analyzed Formula One data.

## Technologies Used

- **Azure Databricks**: For data processing and transformations using PySpark and Spark SQL.
- **Azure Data Lake Storage (ADLS)**: For scalable storage of ingested and transformed data.
- **Azure Data Factory (ADF)**: For pipeline creation, automation, and scheduling.
- **Delta Lake**: For managing incremental loads and data versioning.
- **Power BI**: For visualizing business-ready data.
- **Unity Catalog**: For managing access to data assets.

## Key Features

- **Multi-format data ingestion**: Ingested data in both CSV and JSON formats.
- **Incremental load processing**: Efficient loading and updating of data using Delta Lake.
- **Orchestration and Automation**: Automated data pipelines with ADF and triggers.
- **Governance and Security**: Managed data access using Unity Catalog.

## Setup and Execution

### Prerequisites

- **Azure Subscription**: Required for deploying Azure Databricks, ADLS, and ADF.
- **Power BI Desktop**: Required for creating and viewing dashboards.

### Steps

1. **Provision Azure Resources**:
   - Set up an **Azure Databricks** workspace.
   - Create an **ADLS** Gen2 account for data storage.
   - Set up **ADF** for orchestrating pipelines.
   - Enable **Unity Catalog** for data governance.

2. **Data Ingestion**:
   - Use ADF pipelines to ingest data from CSV and JSON sources into the **ADLS Raw Layer**.

3. **Data Transformation**:
   - Use **Azure Databricks** notebooks to clean, transform, and prepare data using **PySpark**.
   - Store transformed data in the **ADLS Ingested Layer**.

4. **Data Orchestration**:
   - Create **ADF pipelines** for scheduling the ingestion and transformation tasks.
   - Implement triggers in ADF for automating pipelines.

5. **Data Versioning**:
   - Enable **Delta Lake** to manage incremental loads and data versions.

6. **Data Analysis**:
   - Load data into **Power BI** from the ADLS Presentation Layer.
   - Create Power BI reports and dashboards for data visualization.

## Conclusion

This project demonstrates how to integrate Azure Databricks with other Azure services like ADLS, ADF, and Power BI to build a scalable data pipeline for analyzing Formula One data. The use of PySpark and Spark SQL for transformation, along with Delta Lake and Unity Catalog for data management, ensures efficient and secure data processing.
