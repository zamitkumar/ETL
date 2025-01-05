# ETL
Disaster Response Classification Project

ETL Pipeline Preparation 
Objective:
This project aims to create an ETL (Extract, Transform, Load) pipeline for processing disaster response data. The following steps outline how to build the pipeline and prepare the data for further analysis or machine learning tasks.

Steps:
1. Import Libraries and Load Datasets
Import the necessary Python libraries.
Load messages.csv into a pandas DataFrame and inspect the first few rows.
Load categories.csv into a pandas DataFrame and inspect the first few rows.
2. Data Cleaning and Transformation
Merge the messages and categories datasets based on the id column.
Clean the categories column by splitting it into individual category columns and converting values to binary (0 or 1).
Drop the original categories column and add the cleaned category columns.
Remove duplicate rows from the merged dataset.
Handle missing values by filling them with the most frequent value for categorical columns and with the median for numerical columns.
3. Save Clean Dataset into SQLite Database
Create a connection to an SQLite database using SQLAlchemy.
Save the cleaned DataFrame into an SQLite database as a table named DisasterMessages.
4. Create process_data.py Script
Create a Python script (process_data.py) that automates the above steps:
Load data from messages.csv and categories.csv.
Clean the data as described above.
Save the cleaned data into an SQLite database.
Final Output:
The cleaned data will be saved in a SQLite database (DisasterResponse.db) with the DisasterMessages table ready for further analysis or model training.
