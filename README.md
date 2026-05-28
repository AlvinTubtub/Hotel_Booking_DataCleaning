# Hotel Booking Data Cleaning and Analysis

This repository contains a data cleaning pipeline and an Exploratory Data Analysis (EDA) for the "Hotel Booking" dataset, implemented in Python.

## Overview
The goal of this project is to prepare raw hotel booking data for analysis by handling missing values and feature engineering, followed by a comprehensive visualization of booking trends and cancellation behaviors.

## Key Data Cleaning Steps
The `DataCleaning-1.ipynb` notebook performs the following operations:
* **Renaming Columns**: Standardized naming for better readability (e.g., `adults` to `num_adults`).
* **Handling Missing Values**: 
    * Imputed missing `agent` values with -1.
    * Labeled missing `country` entries as 'Unknown'.
    * Removed rows with missing `num_children` data.
* **Data Transformation**: 
    * Dropped the `company` column due to high sparsity.
    * Converted columns such as `is_canceled` and `is_repeated_guest` to `boolean` types.
* **Feature Engineering**: 
    * Created `lead_time_binned` to group booking lead times into categorical ranges.
* **Data Quality**: 
    * Cleaned string inconsistencies in the `hotel` column and removed all duplicate records.

## Key Analytical Insights
Following the cleaning process, an EDA was conducted to visualize core business metrics:
* **Seasonal Booking Trends**: Monthly visualization of visitor volume identifies peak demand periods, allowing for better operational planning.
* **Hotel Type Comparison**: A side-by-side comparison of "Resort Hotel" vs. "City Hotel" bookings reveals differences in market volume.
* **Cancellation Analysis**: 
    * Evaluated cancellation rates by hotel type to identify risk factors.
    * Analyzed the impact of **Lead Time** on cancellations, revealing that longer lead times are strongly correlated with higher cancellation rates.
    * Examined **Deposit Types**, finding that payment policies significantly influence the likelihood of a booking being canceled.

## Requirements
* Python 3
* `pandas`
* `matplotlib`
* `seaborn`
