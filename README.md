# MyFirstSQLProject
My first SQL project focused on practicing SQL queries, data analysis, filtering, sorting, grouping, joins, and other fundamental SQL concepts.
# 📚 MyFirstSQLProject – Online Bookstore Database

## 📌 Project Overview

This is my first practical SQL project, based on an **Online Bookstore Database** created using **PostgreSQL**.

The project focuses on creating a relational database for an online bookstore and performing SQL-based analysis on **books, customers, and orders**.

The database is named `OnlineBookstore` and contains three main tables:

- **Books** – Stores information about books, including title, author, genre, published year, price, and stock.
- **Customers** – Stores customer information such as name, email, phone, city, and country.
- **Orders** – Stores information about customer orders, including the customer, book, order date, quantity, and total amount.

The project includes both **basic and advanced SQL queries** to retrieve and analyze the data.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Create a database using PostgreSQL.
- Create relational tables with primary and foreign keys.
- Import data into the database.
- Retrieve and filter records using SQL.
- Sort and limit query results.
- Perform calculations using aggregate functions.
- Use `GROUP BY` and `HAVING` for data analysis.
- Combine multiple tables using `JOIN`.
- Analyze book sales and inventory.
- Analyze customer orders and spending.
- Practice writing SQL queries for real-world business scenarios.

---

## 🗄️ Database Structure

The project contains three main tables.

### 1. Books

The `Books` table stores information about books available in the bookstore.

| Column | Description |
|---|---|
| `Book_ID` | Unique ID of the book |
| `Title` | Title of the book |
| `Author` | Author of the book |
| `Genre` | Genre of the book |
| `Published_Year` | Year the book was published |
| `Price` | Price of the book |
| `Stock` | Available stock |

`Book_ID` is the primary key of the table.

---

### 2. Customers

The `Customers` table stores information about bookstore customers.

| Column | Description |
|---|---|
| `Customer_ID` | Unique ID of the customer |
| `Name` | Customer name |
| `Email` | Customer email |
| `Phone` | Customer phone number |
| `City` | Customer city |
| `Country` | Customer country |

`Customer_ID` is the primary key of the table.

---

### 3. Orders

The `Orders` table stores information about customer purchases.

| Column | Description |
|---|---|
| `Order_ID` | Unique ID of the order |
| `Customer_ID` | ID of the customer who placed the order |
| `Book_ID` | ID of the ordered book |
| `Order_Date` | Date of the order |
| `Quantity` | Number of books ordered |
| `Total_Amount` | Total order amount |

`Order_ID` is the primary key.

The `Customer_ID` and `Book_ID` columns are foreign keys that connect the `Orders` table with the `Customers` and `Books` tables.

---

## 🔗 Database Relationships

The tables are connected using primary and foreign keys.

```text
Customers
    │
    │ Customer_ID
    ▼
Orders
    │
    │ Book_ID
    ▼
Books
```

These relationships allow information from different tables to be combined for analysis.

For example:

- Identify which customer placed an order.
- Identify which book was ordered.
- Calculate customer spending.
- Calculate books sold by genre.
- Calculate books sold by author.
- Calculate remaining stock.

---

## 📥 Data Import

The project uses CSV files to import data into the PostgreSQL tables.

The SQL script contains data import commands for:

- `Books.csv`
- `Customers.csv`
- `Orders.csv`

The PostgreSQL `COPY` command is used to load the CSV data into the respective tables.

---

# 🔍 SQL Analysis

The project contains two levels of SQL analysis:

## 🟢 Basic SQL Analysis

The basic queries focus on retrieving and filtering information from individual tables.

Examples include:

- Retrieve all books from the **Fiction** genre.
- Find books published after **1950**.
- Find customers from **Canada**.
- Retrieve orders placed during **November 2023**.
- Calculate the total available book stock.
- Find the most expensive book.
- Find orders where the quantity is greater than 1.
- Find orders with a total amount greater than $20.
- Retrieve all available book genres.
- Find the book with the lowest stock.
- Calculate total revenue from orders.

These queries helped me practice fundamental SQL commands such as:

`SELECT`, `WHERE`, `BETWEEN`, `DISTINCT`, `ORDER BY`, `LIMIT`, and aggregate functions.

---

## 🔵 Advanced SQL Analysis

The advanced queries combine multiple tables and perform grouped analysis.

Examples include:

### Sales by Genre

Calculate the total number of books sold for each genre by joining the `Orders` and `Books` tables.

### Average Book Price

Calculate the average price of books belonging to the **Fantasy** genre.

### Customer Order Analysis

Identify customers who have placed at least two orders using `JOIN`, `COUNT()`, `GROUP BY`, and `HAVING`.

### Most Frequently Ordered Book

Find the book that appears in the highest number of orders.

### Top Fantasy Books

Retrieve the top three most expensive books in the Fantasy genre.

### Sales by Author

Calculate the total quantity of books sold by each author.

### Customer Spending

Identify the customer who spent the most based on their total order amount.

### Remaining Stock

Compare the original book stock with ordered quantities to calculate the remaining quantity.

---

## 🛠️ SQL Concepts Practiced

Through this project, I practiced the following PostgreSQL concepts:

- Database creation
- Table creation
- Primary Keys
- Foreign Keys
- Data import using `COPY`
- `SELECT`
- `WHERE`
- `BETWEEN`
- `DISTINCT`
- `ORDER BY`
- `LIMIT`
- `SUM()`
- `AVG()`
- `COUNT()`
- `GROUP BY`
- `HAVING`
- `JOIN`
- `LEFT JOIN`
- `COALESCE()`
- Date filtering
- Aggregate functions
- Relational database concepts

---

## 🧠 What I Learned

This project helped me understand how SQL can be used for practical data analysis rather than only retrieving individual records.

Through this project, I practiced how to:

- Create and structure relational database tables.
- Establish relationships using primary and foreign keys.
- Import external data into PostgreSQL.
- Filter and sort data.
- Perform calculations using aggregate functions.
- Combine information from multiple tables using joins.
- Group data for analysis.
- Filter grouped results using `HAVING`.
- Analyze customer orders and spending.
- Analyze book sales by genre and author.
- Calculate inventory remaining after orders.

---

## ⚠️ PostgreSQL Case Sensitivity

One important point noted while working on this project is the handling of text values in filtering conditions.

For example:

```sql
SELECT *
FROM Customers
WHERE Country = 'Canada';
```

The value used in the condition needs to correspond to the stored text value. A differently cased value such as `'CANADA'` should not be assumed to match `'Canada'` in a normal text comparison.

This was one of the PostgreSQL behaviors noted during the project.

---

## 🚀 Future Improvements

Some possible improvements for this project are:

- Perform monthly sales analysis.
- Analyze revenue by genre.
- Identify the best-selling authors.
- Analyze customer spending patterns.
- Calculate average order value.
- Analyze sales by country and city.
- Create SQL views for frequently used reports.
- Add more advanced queries using subqueries and CTEs.
- Connect the PostgreSQL database with Power BI.
- Create interactive dashboards based on the bookstore data.

---

## 📂 Project Files

```text
MyFirstSQLProject/
│
├── PROJECT10-11-2026.sql
└── README.md
```

### `PROJECT10-11-2026.sql`

Contains the complete SQL code for:

- Database creation
- Table creation
- Data import
- Basic SQL queries
- Advanced SQL queries
- Book, customer, order, sales, and inventory analysis

### `README.md`

Contains the project documentation, database structure, SQL concepts practiced, and project learning outcomes.

---

## 📌 Conclusion

This project represents my first practical SQL project using PostgreSQL.

It helped me build a foundation in relational database concepts and SQL-based data analysis by working with books, customers, and orders.

Through this project, I practiced moving from **basic data retrieval to multi-table analysis and business-oriented queries**.

This project is also a starting point for developing further skills in **SQL, Data Analysis, Business Intelligence, and database-driven reporting**.
