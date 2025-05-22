
# 📊 SQL Data Warehouse Analytics Project

This repository contains a comprehensive set of SQL scripts designed to build and analyze a data warehouse for business insights. It follows a structured approach, from database setup to dimensional modeling, and advanced analytical queries.

---

## 🏗️ 0. Initialization – `00_init_database.sql`

Creates the `DataWarehouseAnalytics` database and the `gold` schema. It sets up three core tables:

- `dim_customers`
- `dim_products`
- `fact_sales`

⚠️ **Warning**: This script drops the database if it exists. Ensure backups before running.

---

## 🔍 1. Database Exploration – `01_database_exploration.sql`

- Lists all tables and views in the database using `INFORMATION_SCHEMA.TABLES`
- Describes the structure of the `dim_customers` table using `INFORMATION_SCHEMA.COLUMNS`

---

## 📐 2. Dimensions Exploration – `02_dimensions_exploration.sql`

Explores dimension tables:

- Unique `country` values in `dim_customers`
- Unique combinations of `category`, `subcategory`, and `product_name` in `dim_products`

---

## 📅 3. Date Range Analysis – `03_date_range_exploration.sql`

Assesses date-related insights:

- Minimum and maximum `order_date` values from `fact_sales`
- Age range of customers based on `birthdate`

---

## 📏 4. Measures & KPIs – `04_measures_exploration.sql`

Calculates high-level metrics such as:

- Total sales, quantity, and orders
- Average selling price
- Number of unique products and active customers
- Business summary report via `UNION ALL`

---

## 📊 5. Magnitude Analysis – `05_magnitude_analysis.sql`

Groups and quantifies metrics:

- Customers by country and gender
- Products by category
- Average cost per category
- Revenue by product category and customer
- Distribution of sold items across countries

---

## 🏅 6. Ranking Analysis – `06_ranking_analysis.sql`

Identifies top and bottom performers using `RANK()`, `TOP`, and `ROW_NUMBER()`:

- Top 5 revenue-generating products
- Bottom 5 worst-performing products
- Top 10 highest-spending customers
- Bottom 3 customers by number of orders

---

## 📂 Folder Structure

```
.
├── 00_init_database.sql
├── 01_database_exploration.sql
├── 02_dimensions_exploration.sql
├── 03_date_range_exploration.sql
├── 04_measures_exploration.sql
├── 05_magnitude_analysis.sql
└── 06_ranking_analysis.sql
```

---

## 💡 Requirements

- Microsoft SQL Server
- Management tool (e.g., SSMS)
- CSV data located at `C:\sql\sql-data-analytics-project\datasets\csv-files\`

---

## 🧠 Author Notes

This project demonstrates foundational and advanced SQL techniques for data warehousing and business analytics. It's an ideal learning tool or foundation for more complex BI pipelines.


