🌐 Covid-19 Prediction and Reporting with Azure Data Factory




Welcome to the Covid-19 Prediction and Reporting project repository! This project leverages Azure Data Factory to build a comprehensive data pipeline for ingesting, transforming, and analyzing Covid-19 data.

🚀 Overview

This project aims to predict and report Covid-19 trends using various Azure services, providing a robust solution for data scientists and analysts.

🔧 Features
Data Integration: Ingest data from multiple sources including ECDC and Eurostat.
Data Transformation: Clean and transform data for analysis.
Data Storage: Utilize Azure Data Lake Storage Gen2 and Azure SQL Database.
Data Analysis: Implement machine learning models to predict trends.
Reporting: Visualize data with PowerBI.
🛠 Technologies
 Azure Data Factory
 Azure SQL Database
 Azure Blob Storage
 Azure Data Lake Storage Gen2
 Azure Databricks
 PowerBI
📂 Getting Started

📋 Prerequisites
Basic knowledge of SQL
Azure account setup
🛠 Installation
Clone the repository.
bash
Copy code
git clone https://github.com/yourusername/covid19-prediction-reporting.git
cd covid19-prediction-reporting
Set up the Azure environment by following the course modules.
Install the required Python packages.
bash
Copy code
pip install -r requirements.txt
📚 Course Structure

Environment Setup
Creating Azure Free Account
Setting up Azure Storage
Configuring Azure Data Factory
Data Ingestion
Ingesting data from Blob Storage
Using HTTP Connector
Sample Ingestion Code:
python
Copy code
import azure.datalake.store
# Code to connect and ingest data
Data Flow
Data Preparation with Azure Data Factory
Transformations and Activities
Sample Data Flow:
python
Copy code
# Sample data flow configuration
Analysis
Analyzing data with Azure Databricks
Implementing Machine Learning Models
Sample Analysis Code:
python
Copy code
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("Covid19Analysis").getOrCreate()
# Code for data analysis
Orchestration
Pipeline Monitoring and Management
CI/CD Integration
Reporting
Creating Dashboards with PowerBI
