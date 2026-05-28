Hotel Booking Data Cleaning
This repository contains a data cleaning pipeline for the "Hotel Booking" dataset, implemented in Python using the pandas library.

Overview
The goal of this project is to prepare raw hotel booking data for further analysis by handling missing values, standardizing column names, removing duplicates, and performing feature engineering.

Key Cleaning Steps
The DataCleaning-1.ipynb notebook performs the following operations:

Renaming Columns: Improves readability (e.g., adults to num_adults).

Handling Missing Values:

Fills missing values in the agent column with -1.

Fills missing values in the country column with 'Unknown'.

Removes rows with missing num_children values.

Data Transformation:

Drops the company column due to excessive missing data.

Updates data types for columns like is_canceled and is_repeated_guest to boolean for better memory efficiency and analysis.

Feature Engineering:

Creates a new column lead_time_binned by binning the lead_time variable into categorical ranges.

Data Quality:

Cleans string data in the hotel column.

Identifies and removes duplicate records from the dataset.

Requirements
Python 3

pandas library
