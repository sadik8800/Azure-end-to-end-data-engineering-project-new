# 🚕 End-to-End Azure Data Engineering Project – NYC Taxi Data

An end-to-end data engineering and analytics project built using **Microsoft Azure** and **Databricks**, using NYC Taxi trip data as the source. The project demonstrates how raw data can be ingested from an API, stored in Azure Data Lake Storage, transformed using PySpark, managed as Delta Lake tables, and finally visualized through a Power BI dashboard.

---

## 📌 Project Overview

The goal of this project is to build an **end-to-end analytics pipeline** for NYC Taxi data using modern cloud data engineering technologies.

The pipeline starts by fetching NYC Taxi data through an API using **Azure Data Factory (ADF)**. The raw data is then stored in the **Bronze/Raw layer of Azure Data Lake Storage Gen2 (ADLS Gen2)**.

The data is subsequently processed and transformed using **Azure Databricks and PySpark**. The transformed data is stored as **Delta Lake tables** and queried using **Databricks SQL**.

Finally, **Power BI** connects to Databricks SQL to create interactive dashboards and visualize insights from the processed NYC Taxi data.

### End-to-End Data Flow

```text
NYC Taxi Data API
       │
       ▼
Azure Data Factory
       │
       │ API Ingestion
       ▼
Azure Data Lake Storage Gen2
Bronze / Raw Layer
       │
       ▼
Azure Databricks
PySpark Transformations
       │
       ▼
Delta Lake Tables
       │
       ▼
Databricks SQL
       │
       ▼
Power BI Dashboard
```

---

## 🏗️ Architecture

```text
                  ┌──────────────────────┐
                  │   NYC Taxi Data API  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Azure Data Factory   │
                  │   Data Ingestion     │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │     ADLS Gen2        │
                  │  Bronze / Raw Data   │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │  Azure Databricks    │
                  │  PySpark Processing  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │    Delta Lake        │
                  │ Transformed Tables   │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   Databricks SQL     │
                  │   Data Analytics     │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │      Power BI        │
                  │ Interactive Dashboard│
                  └──────────────────────┘
```

---

## 🛠️ Technologies Used

| Technology                       | Purpose                                             |
| -------------------------------- | --------------------------------------------------- |
| **Azure Data Factory**           | API-based data ingestion and pipeline orchestration |
| **Azure Data Lake Storage Gen2** | Storage for raw data in the Bronze/Raw layer        |
| **Azure Databricks**             | Data processing and transformation                  |
| **Apache Spark / PySpark**       | Distributed data transformation and processing      |
| **Delta Lake**                   | Storage and management of transformed data          |
| **Databricks SQL**               | Querying and analyzing Delta Lake tables            |
| **Power BI**                     | Data visualization and dashboard development        |

---

## 🔄 Data Pipeline

### 1. Data Source

The project uses **NYC Taxi trip data** as the primary data source.

The data is fetched through an **API**, providing the source data required for the analytics pipeline.

---

### 2. Data Ingestion – Azure Data Factory

**Azure Data Factory (ADF)** is used to ingest data from the NYC Taxi API.

ADF acts as the data ingestion and orchestration layer of the pipeline.

The API data is fetched and loaded into **Azure Data Lake Storage Gen2**.

**Key responsibilities:**

* Connect to the NYC Taxi data API
* Fetch source data
* Transfer raw data to ADLS Gen2
* Store data in the Bronze/Raw layer

---

### 3. Bronze / Raw Layer – ADLS Gen2

The raw API data is stored in the **Bronze/Raw layer** of Azure Data Lake Storage Gen2.

This layer preserves the source data before transformation and processing.

```text
NYC Taxi API
     │
     ▼
Azure Data Factory
     │
     ▼
ADLS Gen2
     │
     └── Bronze / Raw Layer
```

---

### 4. Data Transformation – Azure Databricks

The raw data is processed using **Azure Databricks**.

**PySpark** is used to perform data transformation and processing operations.

The Databricks environment provides a scalable platform for processing the NYC Taxi dataset using Apache Spark.

The transformed data is then stored as **Delta Lake tables**.

```text
Bronze / Raw Data
       │
       ▼
Azure Databricks
       │
       ▼
PySpark Transformations
       │
       ▼
Delta Lake Tables
```

---

### 5. Delta Lake

The processed data is stored in **Delta Lake tables**.

Delta Lake provides a reliable table format for storing and querying processed data within the Databricks environment.

The Delta tables serve as the primary data layer for downstream analytics.

---

### 6. Databricks SQL

**Databricks SQL** is used to query and analyze the Delta Lake tables.

SQL queries can be used to explore the processed NYC Taxi data and prepare the required data for visualization and reporting.

```text
Delta Lake Tables
       │
       ▼
Databricks SQL
       │
       ▼
Analytics & Queries
```

---

### 7. Power BI Dashboard

The final analytics layer is built using **Power BI**.

Power BI is connected to **Databricks SQL**, allowing the processed NYC Taxi data to be visualized through interactive dashboards.

The dashboard provides a visual representation of the data and enables users to explore insights from the NYC Taxi dataset.

```text
Databricks SQL
       │
       ▼
Power BI
       │
       ▼
Interactive Analytics Dashboard
```

---

## ⏱️ Pipeline Execution

The pipeline is **triggered manually when required**.

The workflow can be executed by manually triggering the data ingestion and processing pipeline when new data needs to be processed.

---

## 🎯 Project Objectives

* Build an end-to-end cloud-based data engineering pipeline.
* Ingest NYC Taxi data from an external API.
* Use Azure Data Factory for data ingestion.
* Store raw data in Azure Data Lake Storage Gen2.
* Process data using Azure Databricks and PySpark.
* Store transformed data using Delta Lake.
* Query processed data using Databricks SQL.
* Connect Databricks SQL with Power BI.
* Create an analytics dashboard for data visualization.
* Gain hands-on experience with modern Azure data engineering technologies.

---

## 📊 End-to-End Workflow

```text
1. NYC Taxi API
       ↓
2. Azure Data Factory
       ↓
3. ADLS Gen2 – Bronze/Raw Layer
       ↓
4. Azure Databricks
       ↓
5. PySpark Data Transformations
       ↓
6. Delta Lake Tables
       ↓
7. Databricks SQL
       ↓
8. Power BI Dashboard
```

---

## 📁 Project Structure

```text
nyc-taxi-azure-data-engineering/
│
├── README.md
│
├── adf/
│   └── pipelines/
│
├── databricks/
│   └── notebooks/
│
├── sql/
│   └── queries/
│
├── powerbi/
│   └── screenshots/
│
├── architecture/
│   └── architecture.png
│
└── docs/
    └── project-documentation.md
```

> **Note:** Update the folder structure above according to the actual files and folders included in the repository.

---

## 🚀 Key Learnings

Through this project, I gained practical experience in:

* Building cloud-based data pipelines
* Working with Azure Data Factory
* Ingesting data from APIs
* Using Azure Data Lake Storage Gen2
* Processing large datasets using PySpark
* Working with Delta Lake tables
* Writing analytical queries using Databricks SQL
* Connecting Databricks SQL with Power BI
* Designing an end-to-end data engineering workflow
* Working with Azure cloud data engineering services

---

## 📌 Conclusion

This project demonstrates a complete **end-to-end Azure data engineering workflow**, starting from API-based data ingestion and ending with business intelligence visualization.

The project combines **Azure Data Factory, ADLS Gen2, Azure Databricks, PySpark, Delta Lake, Databricks SQL, and Power BI** to create a modern data pipeline for analyzing NYC Taxi data.

---

## 👨‍💻 Author

**Sadik Saifi**

Aspiring Data Engineer | Python | SQL | PySpark | Databricks | Azure


