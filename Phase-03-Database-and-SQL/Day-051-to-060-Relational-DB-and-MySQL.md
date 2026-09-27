# 🎯 Days 51–60: Relational Databases & MySQL Basics

Walang app na mabubuhay nang walang database! Dito mo matututunan kung paano mag-store, mag-organisa, at mag-query ng structured data gamit ang MySQL.

---

### 📅 Day 51: Relational Database Concepts
- **Konsepto**: Ano ang RDBMS (Relational Database Management System)?
  - Tables (Entities), Rows (Records), Columns (Fields).
  - Primary Key (Unique identifier ng bawat row).
  - SQL vs NoSQL (Bakit SQL ang laging default sa mga kumpanya).
- **Activity**: Mag-drawing ng concept diagram ng isang Paaralan (Students, Courses, Teachers).
- **Output**: `day-51/erd-concept.png` o `.md`

---

### 📅 Day 52: Setting Up MySQL & GUI Tools
- **Konsepto**: Pag-install at pagpapatakbo ng MySQL server.
  - Gamit ang XAMPP (Apache + MySQL) o standalone MySQL Server.
  - GUI Tools: phpMyAdmin, MySQL Workbench, o DBeaver.
- **Activity**: Patakbuhin ang MySQL sa iyong computer at gumawa ng unang database: `CREATE DATABASE fullstack_db;`.
- **Output**: Screenshot ng bukas na database connection.

---

### 📅 Day 53: SQL Data Types & Constraints
- **Konsepto**: Pagpili ng tamang storage type para sa efficiency:
  - Numbers: `INT`, `BIGINT`, `DECIMAL(10, 2)` (Laging DECIMAL para sa pera, huwag FLOAT!).
  - Strings: `VARCHAR(255)`, `TEXT`.
  - Dates: `DATE`, `DATETIME`, `TIMESTAMP`.
  - Constraints: `NOT NULL`, `UNIQUE`, `DEFAULT`, `AUTO_INCREMENT`.
- **Activity**: Isulat ang `CREATE TABLE` query para sa isang `users` table na may id, full_name, email, password_hash, created_at.
- **Output**: `day-53/create-users.sql`

---

### 📅 Day 54: DDL Operations: CREATE, ALTER, DROP
- **Konsepto**: Data Definition Language.
  - `CREATE TABLE`
  - `ALTER TABLE users ADD COLUMN phone_number VARCHAR(20);`
  - `ALTER TABLE users DROP COLUMN phone_number;`
  - `DROP TABLE` vs `TRUNCATE TABLE`.
- **Activity**: Gumawa ng `products` table, magdagdag ng bagong column gamit ang `ALTER`, at i-modify ang data type nito.
- **Output**: `day-54/ddl-practice.sql`

---

### 📅 Day 55: DML Operations: INSERT & Basic SELECT
- **Konsepto**: Data Manipulation Language.
  - `INSERT INTO products (name, price, stock) VALUES ('Laptop', 45000.00, 10);`
  - `SELECT * FROM products;`
  - `SELECT name, price FROM products;`
- **Activity**: Mag-insert ng 10 sample products sa iyong database gamit ang SQL script.
- **Output**: `day-55/seed-products.sql`

---

### 📅 Day 56: Filtering Data with WHERE Clauses
- **Konsepto**: Pagkuha ng specific na mga records:
  - Operators: `=`, `!=`, `>`, `<`, `>=`, `<=`.
  - Logical: `AND`, `OR`, `NOT`.
  - Pattern matching: `LIKE '%phone%'` (Wildcards).
  - Ranges & Sets: `BETWEEN 100 AND 500`, `IN ('Electronics', 'Clothing')`.
  - Null checking: `IS NULL`, `IS NOT NULL`.
- **Activity**: Sumulat ng 5 magkakaibang filter queries sa iyong `products` table.
- **Output**: `day-56/filter-queries.sql`

---

### 📅 Day 57: Sorting & Pagination (ORDER BY, LIMIT, OFFSET)
- **Konsepto**: Paano ginagawa ang page 1, page 2, page 3 sa mga e-commerce sites?
  - `ORDER BY price DESC` (Pinakamahal muna).
  - `LIMIT 10 OFFSET 0` (Page 1: first 10 items).
  - `LIMIT 10 OFFSET 10` (Page 2: next 10 items).
- **Activity**: Sumulat ng pagination query para kunin ang Top 5 cheapest products.
- **Output**: `day-57/pagination.sql`

---

### 📅 Day 58: Safe UPDATE & DELETE Queries
- **Konsepto**: ⚠️ **CRITICAL WARNING**: Huwag na huwag magpapatakbo ng `UPDATE` o `DELETE` nang walang `WHERE` clause sa kumpanya!
  - `UPDATE products SET price = 39999.00 WHERE id = 1;`
  - `DELETE FROM products WHERE stock = 0;`
  - Soft Deletes concept (`is_deleted` o `deleted_at` column).
- **Activity**: I-update ang presyo ng 2 produkto at mag-delete ng 1 test record.
- **Output**: `day-58/update-delete.sql`

---

### 📅 Day 59: SQL Aggregate Functions & GROUP BY
- **Konsepto**: Pagkuha ng mga statistics at summary reports:
  - `COUNT(*)`, `SUM(price)`, `AVG(price)`, `MIN(price)`, `MAX(price)`.
  - `GROUP BY category` (Pagkuha ng total sales o total stock per category).
  - `HAVING COUNT(*) > 5` (Filtering groups).
- **Activity**: Sumulat ng query na nagpapakita ng kabuuang bilang ng produkto at average price bawat kategorya.
- **Output**: `day-59/aggregates.sql`

---

### 📅 Day 60: 🏆 MINI-PROJECT #6 — University / Inventory Database Design
- **Goal**: Gumawa ng standalone SQL script na may kumpletong database schema para sa isang School Inventory System.
- **Requirements**:
  1. Tables: `departments`, `items`, `borrowers`, `transactions`.
  2. Primary keys at valid data types sa bawat column.
  3. Hindi bababa sa 15 rows ng sample mock data (`INSERT`).
  4. 5 analytical queries (e.g. Most borrowed item, Items needing maintenance).
- **Action**: I-commit ang `.sql` file sa inyong GitHub repo.
