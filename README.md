# 🛒 SQL E-Commerce Database Analysis

## 📌 Project Overview
This project demonstrates how SQL can be used to design a relational database and perform analytical queries on an **E-Commerce dataset**.  

The project includes:
- **Database schema** with tables for Products, Customers, Orders, Reviews, and Suppliers
- **Sample dataset** for testing queries
- **Analytical queries** to extract meaningful insights

## 🔧 Tools & Technologies
- SQL
- MySQL / PostgreSQL (compatible)
- ERD (Entity Relationship Design)

## 📂 Files Included
- `SQL PROJECT DATA.sql` → Database schema + sample data
- `Queries.sql` → Business queries for analysis

## 🚀 Key SQL Queries
1. Top 5 Best-Selling Products  
2. Total Revenue by Product Category  
3. Average Rating of Products  
4. Low Stock Alert (Products < 50 units)  
5. Most Active Customers (Highest Orders)  
6. Products with No Reviews  
7. Top Reviewed Products  
8. Customers Who Spent More Than ₹2000  
9. Customers Who Bought More Than 3 Different Products  
10. Products Never Ordered  
11. Average Order Quantity per Product  
12. Monthly Sales Report  
13. Average Customer Age by City  
14. Most Expensive Product in Each Category  

## 📊 Example Query
```sql
-- Top 5 Best-Selling Products
SELECT p.ProductName, SUM(o.Quantity) AS TotalSold
FROM Orders o
JOIN Products p ON o.ProductID = p.ProductID
GROUP BY o.ProductID
ORDER BY TotalSold DESC
LIMIT 5;
