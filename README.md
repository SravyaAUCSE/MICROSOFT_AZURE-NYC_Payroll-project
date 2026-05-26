Azure Data Factory NYC Payroll Project
Project Overview:
  This project demonstrates the implementation of an end-to-end Azure Data Engineering pipeline using Azure Data Factory, Azure SQL Database, Azure Data Lake Storage Gen2,    and Azure Synapse Analytics.
  The project processes NYC Payroll datasets for the years 2020 and 2021 by ingesting, transforming, aggregating, and loading payroll data into Azure SQL Database and         Synapse external tables.

Technologies Used:
  Microsoft Azure
  Azure Data Factory (ADF)
  Azure SQL Database
  Azure Data Lake Storage Gen2 (ADLS Gen2)
  Azure Synapse Analytics
  GitHub
  Project Architecture

Source Systems:
  Azure Data Lake Gen2 CSV Files
  Azure SQL Database Tables

Processing:
  Azure Data Factory Mapping Data Flows
  Data Aggregation and Transformation

Destination:
  Azure SQL Database
  Azure Synapse External Tables
  ADLS Gen2 Staging Storage
  Datasets Used
  Master Data
  AgencyMaster.csv
  EmpMaster.csv
  TitleMaster.csv
  Payroll Data
  nycpayroll_2020.csv
  nycpayroll_2021.csv
  
Linked Services Created:
  Azure Data Lake Storage Gen2 Linked Service
  Azure SQL Database Linked Service

Datasets Created:
  CSV Datasets
  ds_agency_csv
  ds_emp_csv
  ds_title_csv
  ds_payroll2020_csv
  ds_payroll2021_csv
  SQL Datasets
  ds_agency_sql
  ds_emp_sql
  ds_title_sql
  ds_payroll2020_sql
  ds_payroll2021_sql
  ds_summary_sql

  
Data Flows Implemented:
  DF_load_agency
  Loads Agency master data from ADLS Gen2 to Azure SQL Database.
  DF_load_emp
  Loads Employee master data from ADLS Gen2 to Azure SQL Database.
  DF_load_title
  Loads Title master data from ADLS Gen2 to Azure SQL Database.
  DF_load_payroll2020
  Loads NYC Payroll 2020 data from ADLS Gen2 to Azure SQL Database.
  DF_load_payroll2021
  Loads NYC Payroll 2021 data from ADLS Gen2 to Azure SQL Database.
  DF_PAYROLL_summary
  Combines payroll data from 2020 and 2021 using Union transformation and creates a derived column:

    TotalPaid = RegularGrossPaid + TotalOTPaid + TotalOtherPay

   Aggregate transformation is used to summarize payroll information by FiscalYear and AgencyName.

Pipeline Created:
  PL_NYC_Payroll

Pipeline activities:
  Execute DF_load_agency
  Execute DF_load_emp
  Execute DF_load_title
  Execute DF_load_payroll2020
  Execute DF_load_payroll2021
  Execute DF_PAYROLL_summary
  
Data Verification:
Data verification was successfully performed using:
  Azure SQL queries
  Synapse external table queries
  ADLS Gen2 storage verification
  Successful pipeline execution monitoring

SQL Tables Created:
  NYC_Payroll_EMP_MD
  NYC_Payroll_AGENCY_MD
  NYC_Payroll_TITLE_MD
  NYC_Payroll_Data_2020
  NYC_Payroll_Data_2021
  NYC_Payroll_Summary


Features Implemented:
  End-to-end ETL pipeline
  Data ingestion from ADLS Gen2
  Data transformation using Mapping Data Flows
  Aggregation using Derived Column and Aggregate transformations
  Data loading into Azure SQL Database
  Synapse external table verification
  GitHub integration with Azure Data Factory

Project Outcome:
Successfully designed and implemented a cloud-based payroll data processing pipeline using Azure services with automated orchestration, transformation, and verification workflows.

Author:
SRAVYA JAMI.
