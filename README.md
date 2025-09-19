# SQL Data Warehouse Project

## Overview

This repository contains a complete data engineering project for building a modern data warehouse from scratch using SQL Server. The project demonstrates the end-to-end process of data ingestion, cleansing, transformation, and modeling across three layers: Bronze (raw data), Silver (cleansed and transformed data), and Gold (analytics-ready data model). It follows best practices for data warehousing, including version control with Git, stored procedures for ETL processes, and comprehensive documentation.

The project is inspired by a hands-on tutorial and is designed to handle data from CSV sources, ensuring data quality, integrity, and usability for business reporting and analytics.

<img width="891" height="481" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/b2f7cbc5-fc96-4781-b91e-c44afaceff24" />

## Project Structure

The repository is organized as follows:

- datasets/: Contains sample CSV files used for data ingestion.
- documents/: Includes diagrams (e.g., data flow, architecture), data catalogs, and other project documentation.
- scripts/: SQL scripts for creating schemas, tables, stored procedures, and views.
- tests/: Scripts for data quality checks and validation.

README.md: This file, providing project overview and instructions.

## Technologies Used

SQL Server: For database management, schemas, tables, stored procedures, and views.
Git: For version control and collaboration.
SQL Functions: Including window functions (e.g., ROW_NUMBER, LEAD), string manipulations (e.g., TRIM, SUBSTRING), and case statements for data transformations.

No additional libraries or tools are required beyond a standard SQL Server installation.

# Data Layers

## Bronze Layer
The Bronze layer handles raw data ingestion from source systems (e.g., CSV files).

Key Steps:

- Analyze source data for business context, ownership, and technical details.
- Use BULK INSERT for loading CSV data into staging tables.
- Implement full load processes (truncate and insert) with error handling.
- Create stored procedures for data loading, including duration tracking and output messaging.


Scripts: Located in scripts/bronze/.
Tables: Named like CRM_customer_info following conventions.

## Silver Layer
The Silver layer focuses on data cleansing and transformation to address quality issues.

Key Steps:

- Perform data quality checks (e.g., uniqueness, trimming, consistency).
- Handle duplicates, nulls, inconsistencies using SQL functions (e.g., ROW_NUMBER for deduplication, CASE for standardization).
- Apply business rules (e.g., validate sales calculations, handle negative values).
- Load transformed data into Silver tables via stored procedures.


Scripts: Located in scripts/silver/.
Transformations: Includes date range validation, string cleaning, and derived columns.

## Gold Layer
The Gold layer builds a star schema for analytics, integrating data from Silver.

Key Steps:

- Create views for Dimension and Fact tables.
- Generate surrogate keys and perform final transformations.
- Add integrity checks (e.g., primary key uniqueness).
- Ensure data model connectivity for reporting tools.


Scripts: Located in scripts/gold/.
Output: Ready for BI tools like Power BI or Tableau.
