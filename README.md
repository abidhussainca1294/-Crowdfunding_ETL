 -Crowdfunding_ETL


Project Outline: A relational (SQL) database is the final product to be used for the production environment. Data extraction and transformation is performed using 

python with the following packages: pandas, numpy and date time. The cleaned data is loaded into the relational database using pgAdmin for storage and management. 

Free tool QuickDBD ( https://www.quickdatabasediagrams.com/ ) is used for data modelling by sketching an Entity Relationship Diagram of the tables.

An ETL pipeline is developed using Python, Pandas, both Python dictionary methods and regular expressions to extract and transform the data. After transforming the

data, four CSV files are created and are used to create an Entity Relationship Diagram(ERD) and a table schema. Finally, the CSV file data is re uploaded into a 
Postgres database.


Sources of data are within Resources Folder: 

• contacts.xlsx 

• crowdfunding.xlsx


Tools used: 

• Database Type: Relational (SQL) 

• Data Cleaning and Processing: Jupyter Notebook 

• Packages Used: pandas, numpy, datetime 

• Data Loading: pgAdmin for PostgreSQL database


Crowdfunding Data Processing

This repository contains Python code for processing crowdfunding data from an Excel file, extracting information, cleaning, and organizing it, and exporting it as 

CSV files. Below is an overview of the code functionality and how to use it.


Overview

The provided Python script performs the following tasks:

•	Extracts data from an Excel file containing crowdfunding information (crowdfunding.xlsx).

•	Processes the data to create separate CSV files for categories, subcategories, and campaigns.

•	Extracts contact information from another Excel file (contacts.xlsx) and creates a CSV file for contacts.


Dependencies

Pandas

Numpy


Usage

o	The necessary Python dependencies installed.

o	Placed the crowdfunding.xlsx and contacts.xlsx files in a directory named Resources.

o	Run the Python script provided in the repository.

After execution, the script will generate the following CSV files in the Resources directory:

o	category.csv: Contains category information.

o	subcategory.csv: Contains subcategory information.

o	campaign.csv: Contains processed crowdfunding campaign data.

o	contacts.csv: Contains contact information.


File Descriptions

•	crowdfunding.xlsx: Input Excel file containing crowdfunding data.

•	contacts.xlsx: Input Excel file containing contact information.

•	crowdfunding_processing.py: Python script for processing crowdfunding data.


Code Description

The script reads the crowdfunding data from crowdfunding.xlsx and extracts relevant information such as category, subcategory, campaign details, etc.

It processes the data, cleans it, and organizes it into separate DataFrames.

It then creates CSV files for categories, subcategories, campaigns, and contacts.

Contact information is extracted from contacts.xlsx and processed to create a CSV file.


Database Schema

This repository also contains SQL code for creating and defining a relational database schema for managing crowdfunding data. Below is an overview of the database 

schema, table structures, and foreign key constraints.


Overview

The provided SQL script creates the following tables:

•	campaign: Stores information about crowdfunding campaigns.

•	contacts: Stores contact information of individuals associated with campaigns.

•	category: Stores categories of campaigns.

•	subcategory: Stores subcategories of campaigns.


Foreign Key Constraints

Foreign key constraints are added to the campaign table to reference the contacts, category, and subcategory tables based on their respective IDs, and maintain 

referential integrity between tables.


Data Check Queries

After importing CSV data into the tables, the following queries can be used to verify the data:

select * from campaign; (1000 rows)

select * from category; (9 records)

select * from subcategory; (24 records)

select * from contacts; (1000 records)
