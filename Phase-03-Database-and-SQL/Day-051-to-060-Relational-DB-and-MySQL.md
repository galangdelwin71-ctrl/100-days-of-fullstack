# 🎯 Days 51–60: Relational Databases & MySQL Fundamentals

No production software survives without persistent storage. In this phase, you will master storing, organizing, and querying structured data using industry-standard **MySQL**.

---

### 📅 Day 51: Relational Database Architecture
- **Concepts**: What is a Relational Database Management System (RDBMS)?
  - Tables (Entities), Rows (Records), Columns (Attributes).
  - Primary Key: Unique identifier constraint on every row.
  - Why relational SQL remains the global enterprise standard over NoSQL for transactional integrity.
- **Activity**: Draft an Entity-Relationship concept model for a University portal (Students, Courses, Faculty).
- **Deliverable**: `day-51/erd-concept.md`

---

### 📅 Day 52: Setting Up MySQL Server & GUI Clients
- **Concepts**: Initializing a local database server:
  - Running MySQL via XAMPP or standalone MySQL Server instance.
  - Connecting through visual GUI tools: phpMyAdmin, MySQL Workbench, or DBeaver.
- **Activity**: Launch your MySQL server and create your first database: `CREATE DATABASE fullstack_db;`.
- **Deliverable**: Screenshot of active connection and database list.

---

### 📅 Day 53: SQL Data Types & Column Constraints
- **Concepts**: Precision storage design:
  - Numerical: `INT`, `BIGINT`, `DECIMAL(10, 2)` (Always use DECIMAL for currency, never FLOAT!).
  - Text: `VARCHAR(255)`, `TEXT`.
  - Temporal: `DATE`, `DATETIME`, `TIMESTAMP`.
  - Constraints: `NOT NULL`, `UNIQUE`, `DEFAULT`, `AUTO_INCREMENT`.
- **Activity**: Write a `CREATE TABLE` query for a `users` table including id, full_name, email, password_hash, and created_at.
- **Deliverable**: `day-53/create-users.sql`

---

### 📅 Day 54: DDL Mechanics: CREATE, ALTER, DROP
- **Concepts**: Data Definition Language:
  - `CREATE TABLE`.
  - `ALTER TABLE users ADD COLUMN phone VARCHAR(20);`.
  - `ALTER TABLE users MODIFY COLUMN phone VARCHAR(30);`.
  - `DROP TABLE` vs `TRUNCATE TABLE`.
- **Activity**: Create a `products` table, alter it to append a new column, and modify its constraint safely.
- **Deliverable**: `day-54/ddl-practice.sql`

---

### 📅 Day 55: DML Mechanics: INSERT & Basic SELECT
- **Concepts**: Data Manipulation Language:
  - `INSERT INTO products (name, price, stock) VALUES ('Mechanical Keyboard', 2500.00, 15);`.
  - `SELECT * FROM products;`.
  - Column projection: `SELECT name, price FROM products;`.
- **Activity**: Seed your database with 10 sample commercial products using a structured SQL script.
- **Deliverable**: `day-55/seed-products.sql`

---

### 📅 Day 56: Filtering Records with WHERE Clauses
- **Concepts**: Narrowing down query result sets:
  - Comparison operators: `=`, `!=`, `>`, `<`, `>=`, `<=`.
  - Logical operators: `AND`, `OR`, `NOT`.
  - Pattern matching: `LIKE '%pro%'` (Wildcards).
  - Ranges and sets: `BETWEEN 500 AND 2000`, `IN ('Electronics', 'Office')`.
  - Null checks: `IS NULL`, `IS NOT NULL`.
- **Activity**: Write 5 distinct filtering queries targeting specific price ranges, categories, and stock thresholds.
- **Deliverable**: `day-56/filter-queries.sql`

---

### 📅 Day 57: Sorting & Pagination: ORDER BY, LIMIT, OFFSET
- **Concepts**: Implementing page navigation for web apps:
  - `ORDER BY price DESC` (Highest price first).
  - `LIMIT 10 OFFSET 0` (Page 1: items 1–10).
  - `LIMIT 10 OFFSET 10` (Page 2: items 11–20).
- **Activity**: Construct a query that retrieves the Top 5 most expensive products currently in stock.
- **Deliverable**: `day-57/pagination.sql`

---

### 📅 Day 58: Safe UPDATE & DELETE Mutations
- **Concepts**: ⚠️ **CRITICAL ENGINEERING WARNING**: Never execute an `UPDATE` or `DELETE` without a verified `WHERE` clause!
  - `UPDATE products SET price = 2200.00 WHERE id = 1;`.
  - `DELETE FROM products WHERE stock = 0;`.
  - The Soft-Delete design pattern (`is_deleted BOOLEAN DEFAULT FALSE` or `deleted_at TIMESTAMP NULL`).
- **Activity**: Execute targeted price updates and implement a soft-delete column update on dummy records.
- **Deliverable**: `day-58/update-delete.sql`

---

### 📅 Day 59: Aggregations, GROUP BY & HAVING
- **Concepts**: Computing summary metrics and reports:
  - Aggregate functions: `COUNT(*)`, `SUM(price)`, `AVG(price)`, `MIN(price)`, `MAX(price)`.
  - Grouping records: `GROUP BY category_id`.
  - Filtering groups: `HAVING COUNT(*) > 5`.
- **Activity**: Write a query that computes total inventory value and average product cost per category.
- **Deliverable**: `day-59/aggregates.sql`

---

### 📅 Day 60: 🏆 MILESTONE PROJECT #6 — Inventory Database Schema & Scripts
- **Objective**: Author a standalone production-grade SQL script modeling an Equipment and Inventory Management System.
- **Requirements**:
  1. Tables: `departments`, `items`, `borrowers`, `transactions`.
  2. Strict primary keys, constraints, and valid data types.
  3. Seed script containing at least 15 rows of realistic mock data.
  4. 5 analytical queries (e.g., Highest demand items, Overdue borrowed assets).
- **Verification**: Commit the `.sql` schema script to your repository.
