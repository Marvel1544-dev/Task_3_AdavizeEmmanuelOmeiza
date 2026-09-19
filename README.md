# Task 3: SQL Data Analysis

This repository contains my **DecodeLabs Data Analytics Internship – Project 3** work. The project focuses on analyzing an orders and sales dataset with Microsoft SQL Server and practicing fundamental SQL data-analysis techniques.

## Project Overview

The analysis uses a retail orders dataset stored in an Excel workbook. SQL queries are used to explore the data, summarize business performance, and compare products, order statuses, payment methods, and referral sources.

## Repository Contents

| File | Description |
| --- | --- |
| `Dataset for Data Analytics.xlsx` | Source dataset containing order and sales information. |
| `DecodeLabs_Project3_SQL_Analysis.sql` | SQL Server analysis queries for exploring and summarizing the dataset. |

## Dataset Fields Used

The SQL analysis works with fields including:

- `OrderID` — Unique identifier for each order.
- `Date` — Date of the order.
- `Product` — Product purchased.
- `Quantity` — Number of units ordered.
- `TotalPrice` — Total value of the order.
- `OrderStatus` — Current status of the order.
- `PaymentMethod` — Payment method used by the customer.
- `ReferralSource` — Source that referred the customer.

## SQL Analysis Covered

The SQL script demonstrates the following concepts:

1. Selecting and viewing data with `SELECT`.
2. Filtering records with `WHERE`.
3. Sorting results with `ORDER BY`.
4. Counting records by product with `GROUP BY` and `COUNT`.
5. Calculating total sales with `SUM`.
6. Calculating average sales with `AVG`.
7. Filtering grouped results with `HAVING`.
8. Calculating each product's percentage contribution to total sales.
9. Summarizing orders by order status.
10. Comparing average order value by payment method.
11. Comparing total sales by payment method.
12. Analyzing sales, order count, and average order value by referral source.

## Requirements

- Microsoft SQL Server or another SQL Server-compatible database environment
- SQL Server Management Studio (SSMS), Azure Data Studio, or an equivalent SQL client
- The Excel dataset imported into a database named `DecodeLabs_Project3`

## Database Setup

1. Create a database named `DecodeLabs_Project3`.
2. Import `Dataset for Data Analytics.xlsx` into the database.
3. Ensure the imported table is named `Sheet1$`, or update the table name in the SQL script.
4. Open `DecodeLabs_Project3_SQL_Analysis.sql` in your SQL client.
5. Execute the queries individually or as a complete script.

The script begins with:

```sql
USE DecodeLabs_Project3;
```

## Example Analysis

The project includes queries such as the following to calculate sales by product:

```sql
SELECT
    Product,
    SUM(TotalPrice) AS TotalSales
FROM dbo.Sheet1$
GROUP BY Product
ORDER BY TotalSales DESC;
```

## Learning Objectives

This project demonstrates practical experience with:

- Relational data exploration
- SQL filtering and sorting
- Aggregation and grouped analysis
- Sales and customer-behavior analysis
- Percentage calculations using subqueries
- Translating raw data into useful business insights

## Author

**Adavize Emmanuel Omeiza**

Completed as part of the DecodeLabs Data Analytics Internship.
