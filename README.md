# SQL Data Warehouse Project

## Overview

This repository contains a complete data engineering project for building a modern data warehouse from scratch using SQL Server. The project demonstrates the end-to-end process of data ingestion, cleansing, transformation, and modeling across three layers: Bronze (raw data), Silver (cleansed and transformed data), and Gold (analytics-ready data model). It follows best practices for data warehousing, including version control with Git, stored procedures for ETL processes, and comprehensive documentation.

The project is inspired by a hands-on tutorial and is designed to handle data from CSV sources, ensuring data quality, integrity, and usability for business reporting and analytics.

<img width="891" height="481" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/b2f7cbc5-fc96-4781-b91e-c44afaceff24" />

## Project Structure

The repository is organized as follows:

datasets/: Contains sample CSV files used for data ingestion.
documents/: Includes diagrams (e.g., data flow, architecture), data catalogs, and other project documentation.
scripts/: SQL scripts for creating schemas, tables, stored procedures, and views.
tests/: Scripts for data quality checks and validation.
README.md: This file, providing project overview and instructions.

## Technologies Used

SQL Server: For database management, schemas, tables, stored procedures, and views.
Git: For version control and collaboration.
SQL Functions: Including window functions (e.g., ROW_NUMBER, LEAD), string manipulations (e.g., TRIM, SUBSTRING), and case statements for data transformations.

No additional libraries or tools are required beyond a standard SQL Server installation.
