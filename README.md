🛒 E-commerce Sales Analysis (SQL Project)

📌 Project Overview

This project demonstrates how to analyze e-commerce sales data using SQL.
The goal is to track revenue trends, product performance, and customer purchases through SQL queries.

🗄️ Database & Tables:
Database: e_commerce_sales_analysis
Table: orders

| Column       | Type        | Description                             |
| ------------ | ----------- | --------------------------------------- |
| order\_id    | INT (PK)    | Unique order identifier                 |
| customer\_id | INT         | Unique customer identifier              |
| product      | VARCHAR(50) | Product name                            |
| category     | VARCHAR(50) | Product category (Electronics, Fashion) |
| order\_date  | DATE        | Date when the order was placed          |
| quantity     | INT         | Number of units ordered                 |
| price        | DECIMAL     | Price per unit                          |


📊 Sample Data:

INSERT INTO orders VALUES

(1, 101, 'Laptop', 'Electronics', '2024-01-05', 1, 55000),

(2, 102, 'Headphones', 'Electronics', '2024-01-10', 2, 2000),

(3, 103, 'Shoes', 'Fashion', '2024-02-02', 1, 2500),

(4, 101, 'Mobile', 'Electronics', '2024-02-15', 1, 20000),

(5, 104, 'T-shirt', 'Fashion', '2024-03-01', 3, 800);

📈 Analysis Performed:

🔹 1. Top 5 Best-Selling Products (by Revenue)
SELECT product, SUM(quantity*price) AS revenue
FROM orders
GROUP BY product
ORDER BY revenue DESC
LIMIT 5;


👉 Output: Shows the products generating the highest revenue.

🔹 2. Monthly Revenue Trends
SELECT DATE_FORMAT(order_date, '%Y-%m') AS month, SUM(quantity*price) AS revenue
FROM orders
GROUP BY month
ORDER BY month;


👉 Output: Displays month-wise revenue performance.

🔹 3. View All Orders
SELECT * FROM orders;


👉 Output: Lists all order details in the dataset.

🛠️ Tools & Technologies:

SQL (MySQL / MariaDB / PostgreSQL) – Querying and analysis

Database Schema Design – Orders table for sales records

Data Aggregation – Using SUM(), GROUP BY, ORDER BY, and DATE_FORMAT()

📸 Sample Output :

Top Products: Laptop, Mobile, Headphones, Shoes, T-shirt

Monthly Revenue:

Jan 2024 → ₹59,000

Feb 2024 → ₹22,500

Mar 2024 → ₹2,400


✍️ Author: Surbhi Masih
