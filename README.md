# Walmart Sales Data Analytics

## Project Overview

This project involves analyzing sales data from Walmart to uncover key insights and trends. The analysis covers various aspects such as product performance, customer behavior, and sales distribution across different time periods and locations.

## Database Setup

Ensure you have created and selected the `walmartSales` database. The table structure for the `sales` table is defined as follows:


CREATE TABLE IF NOT EXISTS sales(
    invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
    branch VARCHAR(5) NOT NULL,
    city VARCHAR(30) NOT NULL,
    customer_type VARCHAR(30) NOT NULL,
    gender VARCHAR(30) NOT NULL,
    product_line VARCHAR(100) NOT NULL,
    unit_price DECIMAL(10,2) NOT NULL,
    quantity INT NOT NULL,
    tax_pct FLOAT(6,4) NOT NULL,
    total DECIMAL(12, 4) NOT NULL,
    date DATETIME NOT NULL,
    time TIME NOT NULL,
    payment VARCHAR(15) NOT NULL,
    cogs DECIMAL(10,2) NOT NULL,
    gross_margin_pct FLOAT(11,9),
    gross_income DECIMAL(12, 4),
    rating FLOAT(2, 1)
);

## Data Import

The data for this project is sourced from the `walmartsales.csv` file. Ensure that you have loaded this CSV data into the `sales` table.


## Data Manipulation
The following columns are added to the sales table for further analysis:

time_of_day: Indicates the time of day based on the time column.
day_name: Indicates the day of the week based on the date column.
month_name: Indicates the month based on the date column.

## Analysis Queries
The project includes various SQL queries to analyze the sales data. These queries cover general analysis, customer analysis, and specific insights such as:

-Number of unique cities
-Most selling product line
-Total revenue by month
-Month with the largest COGS
-Product line with the largest revenue
-City with the largest revenue
-Product line with the largest VAT
-Performance of product lines
-Branch performance
-Product line by gender
-Average rating by product line
-Unique customer types
-Unique payment methods
-Most common customer type
-Gender distribution and performance
-Sales by time of day and day of the week
-Customer type bringing most revenue
-City with the largest tax percent
-Customer type paying most VAT
