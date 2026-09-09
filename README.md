# Databricks Data Engineering Project

Data Engineering project built with **Databricks** using the **Lakehouse architecture** and **Medallion Architecture** to process raw e-commerce data and transform it into clean and business-ready datasets.

The project follows a typical data engineering workflow, starting with raw CSV files and progressively transforming them through the **Bronze, Silver and Gold layers**.

## Project Overview

The main goal of the project is to demonstrate how raw data can be ingested, cleaned, transformed and prepared for analytical use inside Databricks.

The pipeline follows this structure:

**Raw CSV Data → Bronze → Silver → Gold → Analytics**

## Architecture & Orchestration

The project follows the **Medallion Architecture** and is orchestrated using Databricks Workflows/Jobs:

<img width="880" height="427" alt="image" src="https://github.com/user-attachments/assets/569472ab-5654-44a2-aa07-f361047fec19" />

### Bronze Layer

The Bronze layer contains the raw data ingested from CSV files.

The data is stored with minimal transformations in order to preserve the original information and provide a reliable source for further processing.

### Silver Layer

The Silver layer contains cleaned and structured data.

Transformations include:

* Data cleaning
* Data type corrections
* Handling missing values
* Removing invalid or unnecessary records
* Structuring the datasets for further processing

This layer acts as the main trusted and cleaned version of the data.

### Gold Layer

The Gold layer contains business-ready datasets created from the cleaned Silver data.

Different datasets are joined and transformed to produce information that can be directly used for analysis and reporting.

This layer focuses on creating meaningful and reusable data products rather than simply storing cleaned data.

---

## Project Structure & Notebooks

The pipeline is organized across several Databricks notebooks, covering individual transformations for each source entity as well as overall layer orchestrations:

<img width="1206" height="722" alt="image" src="https://github.com/user-attachments/assets/ababf4f4-3431-4e07-842e-de60373b61e0" />

---

## Technologies

* **Databricks**
* **Apache Spark**
* **PySpark**
* **SQL**
* **Delta Lake**
* **Lakehouse Architecture**
* **Medallion Architecture**
* **CSV**
* **Git / GitHub**

## Data Engineering Concepts

This project demonstrates several important Data Engineering concepts:

* Data ingestion
* ETL / ELT
* Data cleaning and transformation
* Schema enforcement
* Data joins
* Delta Tables
* Lakehouse architecture
* Medallion architecture
* Bronze, Silver and Gold layers
* Data quality
* Data modeling
* Data preparation for analytics

## Project Workflow

The pipeline can be summarized as:

1. Raw CSV files are loaded into Databricks.
2. The raw data is stored in the Bronze layer.
3. Data is cleaned and validated in the Silver layer.
4. Different datasets are joined and transformed in the Gold layer.
5. The resulting datasets are stored as Delta Tables.
6. The Gold layer provides structured data ready for analytical use.

## What I Learned

Through this project, I gained practical experience with building a data pipeline in Databricks and understanding how data moves from raw files to structured datasets.

The project helped reinforce concepts such as **PySpark transformations, Delta Tables, data quality, Lakehouse architecture and the Medallion Architecture**, which are commonly used in modern Data Engineering environments.
