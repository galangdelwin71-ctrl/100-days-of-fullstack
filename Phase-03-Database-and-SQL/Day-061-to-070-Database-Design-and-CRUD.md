# 🎯 Days 61–70: Schema Design, Joins & Advanced SQL

In this module, you will master multi-table relationships, database normalization, and query optimization patterns tested in technical interviews.

---

### 📅 Day 61: Foreign Keys & Relational Cardinality
- **Concepts**: Establishing relational constraints between tables:
  - Foreign Key (FK) constraints: `FOREIGN KEY (category_id) REFERENCES categories(id)`.
  - **One-to-One (1:1)**: User <-> UserProfile.
  - **One-to-Many (1:N)**: Department <-> Employees.
  - **Many-to-Many (N:M)**: Students <-> Courses (requires a Junction/Pivot table).
- **Activity**: Create a `categories` table and bind it to `products` via a foreign key constraint.
- **Deliverable**: `day-61/foreign-keys.sql`

---

### 📅 Day 62: Database Normalization (1NF, 2NF, 3NF)
- **Concepts**: Eliminating data redundancy and update anomalies:
  - **1NF**: Atomic values (no comma-separated strings inside a single cell).
  - **2NF**: All non-key columns depend on the entire primary key.
  - **3NF**: No transitive dependencies (non-key columns must not depend on other non-key columns).
- **Activity**: Take a denormalized spreadsheet export and normalize it into 3 clean relational tables meeting 3NF.
- **Deliverable**: `day-62/normalization-case-study.md`

---

### 📅 Day 63: SQL Joins: INNER JOIN vs LEFT JOIN
- **Concepts**: Merging datasets across related tables:
  - `INNER JOIN`: Returns records only when there is a matching row in both tables.
  - `LEFT JOIN`: Returns all rows from the primary table, filling missing foreign matches with `NULL`.
- **Activity**: Retrieve a list of all customers alongside their registered orders using a `LEFT JOIN`.
- **Deliverable**: `day-63/joins-practice.sql`

---

### 📅 Day 64: Multi-Table Joins in Production
- **Concepts**: Real-world commercial queries spanning multiple tables:
  - Joining 4 tables: `orders` -> `order_items` -> `products` -> `customers`.
- **Activity**: Write a query that generates a full order receipt breakdown (Customer Name, Order Date, Item Title, Quantity, Unit Price, Line Total).
- **Deliverable**: `day-64/multi-joins.sql`

---

### 📅 Day 65: Subqueries & Nested Queries
- **Concepts**: Embedding query logic within another query:
  - Subquery in `WHERE`: `WHERE price > (SELECT AVG(price) FROM products)`.
  - Subquery in `FROM` (Derived tables).
- **Activity**: Identify all products priced above the store-wide average price using a nested subquery.
- **Deliverable**: `day-65/subqueries.sql`

---

### 📅 Day 66: Database Indexing & Query Performance
- **Concepts**: Why do database queries slow down as tables grow to 1,000,000 records?
  - Full Table Scan vs Index Seek.
  - Creating indexes: `CREATE INDEX idx_user_email ON users(email);`.
  - Using `EXPLAIN` to diagnose query plans and index usage.
- **Activity**: Profile a slow query using `EXPLAIN`, attach an index to the filtered column, and observe the performance difference.
- **Deliverable**: `day-66/indexing-explain.sql`

---

### 📅 Day 67: Database Transactions & ACID Guarantees
- **Concepts**: How banks and stores prevent data corruption during crashes:
  - **A**tomicity, **C**onsistency, **I**solation, **D**urability.
  - `START TRANSACTION;` -> `UPDATE accounts SET balance = balance - 500 ...` -> `COMMIT;` (or `ROLLBACK;` on error).
- **Activity**: Write a transaction block that decrements inventory stock and inserts an order record atomically.
- **Deliverable**: `day-67/transactions.sql`

---

### 📅 Day 68: SQL Injection Attacks & Prepared Statements
- **Concepts**: The most notorious web security vulnerability:
  - What happens when a malicious user inputs `' OR '1'='1` into a login field?
  - Why string concatenation of user inputs into SQL queries is catastrophic.
  - Prepared statements and parameterized query placeholders (`?`).
- **Activity**: Write a technical security brief explaining the attack vector of SQL injection and the mathematical guarantee of prepared statements.
- **Deliverable**: `day-68/sql-injection-prevention.md`

---

### 📅 Day 69: Database Dumps, Backups & Migrations
- **Concepts**: Moving database schemas and records across development and production environments:
  - CLI exports: `mysqldump -u root -p store_db > backup.sql`.
  - CLI restoration: `mysql -u root -p new_db < backup.sql`.
- **Activity**: Export your local development database to a `.sql` file and restore it into a clean test database.
- **Deliverable**: `day-69/backup-log.txt`

---

### 📅 Day 70: 🏆 MILESTONE PROJECT #7 — Normalized E-Commerce Database Schema
- **Objective**: Design and deliver an enterprise-grade relational database schema for an E-Commerce platform.
- **Required Tables**:
  - `users` (id, email, password_hash, role, created_at)
  - `categories` (id, name, slug)
  - `products` (id, category_id, title, price, stock, is_active)
  - `orders` (id, user_id, total_amount, status, created_at)
  - `order_items` (id, order_id, product_id, quantity, unit_price)
- **Queries to deliver**:
  1. Complete DDL schema script with primary and foreign key constraints.
  2. Sample seed dataset covering all tables.
  3. Monthly Sales Analytics report query using Joins and `GROUP BY`.
  4. Top 3 Best-Selling Products query.
- **Verification**: Commit the schema and query suite to GitHub!
