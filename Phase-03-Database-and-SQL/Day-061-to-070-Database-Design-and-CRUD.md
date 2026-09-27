# 🎯 Days 61–70: Schema Design, Joins & Advanced SQL

Dito ka magiging eksperto sa pag-uugnay ng mga tables (Relationships) at pagsusulat ng kumplikadong queries na hinahanap sa mga technical interviews.

---

### 📅 Day 61: Foreign Keys & Relationships
- **Konsepto**: Paano pinag-uugnay ang magkakaibang tables?
  - Foreign Key (FK) constraint.
  - **One-to-One (1:1)**: User -> UserProfile.
  - **One-to-Many (1:N)**: Customer -> Orders.
  - **Many-to-Many (N:M)**: Students <-> Courses (nangangailangan ng Junction/Pivot table).
- **Activity**: Gumawa ng `categories` table at i-link ang `products` table gamit ang `category_id` foreign key.
- **Output**: `day-61/foreign-keys.sql`

---

### 📅 Day 62: Database Normalization (1NF, 2NF, 3NF)
- **Konsepto**: Paano maiiwasan ang duplicate data at update anomalies?
  - **1NF**: Atomic values (bawal ang comma-separated values sa isang cell).
  - **2NF**: Lahat ng non-key attributes ay nakadepende sa buong primary key.
  - **3NF**: Walang transitive dependencies (bawal ang column na nakadepende sa isa pang non-key column).
- **Activity**: Kumuha ng un-normalized spreadsheet table at i-normalize ito sa tatlong separate tables (3NF).
- **Output**: `day-62/normalization-case-study.md`

---

### 📅 Day 63: SQL Joins: INNER JOIN & LEFT JOIN
- **Konsepto**: Pagsasama ng data mula sa magkaibang tables sa iisang result:
  - `INNER JOIN`: Lumalabas lang kapag may match sa dalawang tables.
  - `LEFT JOIN`: Lumalabas lahat ng records mula sa kaliwa, kahit walang katumbas sa kanan (magiging `NULL`).
- **Activity**: Kumuha ng listahan ng lahat ng Customers kasama ang kanilang mga Orders gamit ang `LEFT JOIN`.
- **Output**: `day-63/joins-practice.sql`

---

### 📅 Day 64: Multi-Table Joins (Joining 3 or more tables)
- **Konsepto**: Sa totoong app, karaniwang 3 hanggang 5 tables ang pinag-sasama:
  - `orders` -> `order_items` -> `products` -> `customers`.
- **Activity**: Sumulat ng query na naglalabas ng complete receipt details (Customer Name, Order Date, Product Name, Quantity, Subtotal).
- **Output**: `day-64/multi-joins.sql`

---

### 📅 Day 65: Subqueries & Nested SELECT Queries
- **Konsepto**: Isang query sa loob ng isa pang query:
  - Subquery sa `WHERE`: `WHERE price > (SELECT AVG(price) FROM products)`
  - Subquery sa `FROM` (Derived tables).
- **Activity**: Hanapin ang lahat ng produkto na mas mahal sa overall average price ng buong store.
- **Output**: `day-65/subqueries.sql`

---

### 📅 Day 66: Database Indexing & Performance
- **Konsepto**: Bakit bumabagal ang database kapag umabot na sa 1,000,000 rows?
  - Full Table Scan vs Index Seek.
  - `CREATE INDEX idx_user_email ON users(email);`
  - B-Tree index fundamentals.
- **Activity**: Gamitin ang `EXPLAIN` keyword sa harap ng iyong query para makita kung gumamit ito ng index o nag-full table scan.
- **Output**: `day-66/indexing-explain.sql`

---

### 📅 Day 67: Database Transactions (ACID Principles)
- **Konsepto**: Paano sinisiguro na hindi mawawala ang pera sa bank transfer kapag nag-brownout sa gitna ng proseso?
  - **A**tomicity, **C**onsistency, **I**solation, **D**urability.
  - `START TRANSACTION;` -> `UPDATE` sender -> `UPDATE` receiver -> `COMMIT;` (o `ROLLBACK;` kung may error).
- **Activity**: Sumulat ng transaction script na nagbabawas ng stock sa inventory at nag-i-insert ng record sa orders table nang sabay.
- **Output**: `day-67/transactions.sql`

---

### 📅 Day 68: SQL Injection Vulnerabilities & Prepared Statements
- **Konsepto**: Ang pinaka-sikat na security exploit sa web history:
  - Ano ang mangyayari kung nag-type ang hacker ng `' OR '1'='1` sa login box?
  - Bakit hindi dapat nag-co-concatenate ng user input sa SQL string?
  - Prepared statements at Parameterized queries (`?` placeholders).
- **Activity**: Sumulat ng maikling documentation na nagpapaliwanag kung paano gumagana ang SQL injection at paano ito puksain.
- **Output**: `day-68/sql-injection-prevention.md`

---

### 📅 Day 69: Database Dumps, Backups & Migrations
- **Konsepto**: Paano mag-lipat ng database mula sa iyong laptop papunta sa cloud server?
  - `mysqldump -u root -p my_db > backup.sql`
  - Importing: `mysql -u root -p new_db < backup.sql`
- **Activity**: I-export ang iyong local database bilang `.sql` file at i-import ito sa bagong database gamit ang terminal o phpMyAdmin.
- **Output**: `day-69/backup-log.txt`

---

### 📅 Day 70: 🏆 MINI-PROJECT #7 — Normalized E-Commerce Database Schema
- **Goal**: Gumawa ng production-ready relational database schema para sa isang kumpletong E-Commerce platform.
- **Tables**:
  - `users` (id, email, password, role)
  - `categories` (id, name, slug)
  - `products` (id, category_id, title, price, stock)
  - `orders` (id, user_id, total_amount, status, created_at)
  - `order_items` (id, order_id, product_id, quantity, unit_price)
- **Queries to deliver**:
  1. Script na nag-i-insert ng test data para sa bawat table.
  2. Query para sa Monthly Sales Report.
  3. Query para sa Top 3 Best-Selling Products gamit ang Joins at Group By.
- **Action**: I-commit ang buong SQL project sa inyong GitHub repo.
