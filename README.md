# Azure Data Pipeline and Transformation for Tokyo Olympics Data

**This repository focuses on the implementation of the end-to-end data integration and transformation for the Tokyo Olympics dataset using Azure Data Factory and Databricks.** 

The project involves:

- **Pipeline Design:** Developed data pipelines using Azure Data Factory to automate data ingestion and synchronization.
- **Data Synchronization:** Configured and executed activities to transfer raw data from HTTP sources to Azure Data Lake Storage Gen2.
- **PySpark-Based Processing:** Utilized Azure Databricks to process and transform data with PySpark, ensuring efficient data cleaning and transformation.

This setup enabled real-time data analysis and visualization, providing valuable insights into Olympic performances.

![image](https://github.com/user-attachments/assets/a06ee37f-e2b4-4998-b87d-957b91f6f5c8)

## Project Overview

This project aims to create a comprehensive, real-time, and interactive platform for visualizing Olympic data. It provides valuable insights for analysts, commentators, and enthusiasts to explore Olympic performances in depth. The final output is a visually appealing and user-friendly dashboard designed to attract attention from potential recruiters and stakeholders.

## Objectives

- **Provide a comprehensive, real-time, and interactive platform** for visualizing Olympic data.
- **Offer insights** that can be used by analysts, commentators, and enthusiasts to explore Olympic performances in depth.
- **Create a visually appealing and user-friendly dashboard** that can attract attention from potential recruiters and stakeholders.

## Technologies & Services

- **Azure Data Factory:** A data integration service for building data pipelines that connect to various sources and destinations.
- **Azure Data Lake Storage:** An object storage service for storing structured and unstructured data.
- **Azure Databricks:** A unified analytics platform integrating Apache Spark for data processing and machine learning.
- **Azure Synapse Analytics:** A data warehouse and analytics service that integrates big data and data warehousing.
- **Power BI:** A tool for creating interactive dashboards and reports.

## Prerequisites

- Basic understanding of Python and SQL.
- An Azure account (set up with a 12-month free trial and $200 credit).

## Steps to Execute the Azure Olympics Project

### 1. Create an Azure Account

1. **Sign Up:**
   - Visit the Azure website and click on "Start free" to create an account.
   - Fill in your details, including a phone number and payment information for verification. You will not be charged as long as you use the $200 credit within 30 days.

2. **Complete Account Setup:**
   - After creating your account, log in to your Azure portal.

### 2. Set Up Azure Storage Account

1. **Create a Storage Account:**
   - Search for "Storage account" in the Azure portal and select it.
   - Click on "Create" and set up your storage account with a unique name (e.g., `tokyo-olympic-data`).
   - Select the nearest region, keep the performance option as "Standard," and use "Locally redundant storage (LRS)" for replication.
   - Enable hierarchical namespace to manage data in a directory-like structure.

2. **Create Containers and Folders:**
   - In your storage account, create a container named `tokyo-olympic-data`.
   - Inside this container, create two folders: `raw-data` and `transformed-data`.

### 3. Set Up Azure Data Factory

1. **Create a Data Factory Instance:**
   - Search for "Data Factory" in the Azure portal and select it.
   - Click on "Create," choose the existing resource group (e.g., `TokyoOlympic`), and name your Data Factory instance (e.g., `tokyo-olympic-df`).
   - Proceed through the configuration steps and click "Create."

2. **Launch Azure Data Factory Studio:**
   - Go to the resources and click "Launch Studio" to open the Data Factory design interface.

### 4. Create and Configure Data Pipelines

1. **Set Up Data Pipeline:**
   - In Azure Data Factory Studio, go to the "Author" tab and create a new pipeline.
   - Build a pipeline to ingest raw data from sources like Kaggle into the `raw-data` folder of Azure Data Lake.

2. **Transform Data:**
   - Use Azure Databricks or Azure Synapse Analytics to process and transform the raw data.
   - Write and execute PySpark or SQL scripts to clean and transform the data, then save it to the `transformed-data` folder.

### 5. Analyze and Visualize Data

1. **Use Azure Synapse Analytics:**
   - Create a Synapse workspace and connect it to your data lake.
   - Write SQL queries to analyze the transformed data and gain insights.

2. **Create Dashboards in Power BI:**
   - Connect Power BI to your Azure Synapse Analytics workspace.
   - Develop interactive dashboards and reports to visualize Olympic performance metrics, medal counts, and other relevant data.

### 6. Monitor and Manage Pipelines

1. **Monitor Pipelines:**
   - In Azure Data Factory Studio, go to the "Monitor" tab to track pipeline status.
   - Check for errors or issues during data ingestion and transformation.

2. **Adjust and Optimize:**
   - Make necessary adjustments to improve performance and efficiency based on monitoring results.

## Project Structure

- **Data Source:** Data from the 2021 Tokyo Olympics, available on Kaggle.
- **Data Pipeline:** Extract, transform, and store data, then analyze using SQL queries and visualization tools.
