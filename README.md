# Superstore-Sales-Analysis

The primary goal of this project is to perform a comprehensive analysis of sales data to extract meaningful insights into sales performance, pinpoint emerging trends, and formulate data-driven business strategies. The aim is to enhance decision-making processes by leveraging valuable information derived from the analysis.

Business problem:
How can the business optimize profits by identifying best performing products, categories, sub-categories, or regions? What are the top performing products and which ones need improvement?

The following steps have been taken for the analysis:
1. The original dataset has been pre-processed using Python to standardize the date columns, check for any missing values etc.
2. The processed dataset was then imported into a new .csv file for analysis
3. In-depth analysis is carried out using PostgreSQL.
4. Visualization of the data is done using PowerBI.


### Query 1: Calculating total sales and profit by year

Net sales and profit is calculated for each year

```sql
SELECT
    EXTRACT(YEAR FROM "Order Date") AS order_year,
    SUM("Sales") AS total_sales,
    SUM("Profit") AS total_profit
FROM store
GROUP BY order_year
ORDER BY order_year;
```
![Net sales and profit by year](Net sales by year.png)
![image](https://github.com/simplyprashant/Superstore-Sales-Analysis/assets/133598264/d688f2e7-4a21-435b-ad02-d504f4df7ff3)

