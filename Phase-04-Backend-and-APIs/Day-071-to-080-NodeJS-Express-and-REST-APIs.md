# 🎯 Days 71–80: Node.js, Express & RESTful API Architecture

Dito ninyo itatayo ang backend server na tatanggap ng requests mula sa frontend, makikipag-usap sa database, at magbabalik ng JSON data.

---

### 📅 Day 71: Node.js Runtime & Server Architecture
- **Konsepto**: Ano ang Node.js? Bakit pwede na nating patakbuhin ang JavaScript sa labas ng browser?
  - Client-Server model review.
  - Node modules (`fs`, `path`, `http`).
  - CommonJS (`require`) vs ES Modules (`import/export`).
- **Activity**: Gumawa ng simpleng Node script na nagbabasa ng file mula sa disk at nagpapakita ng laman sa terminal.
- **Output**: `day-71-node/index.js`

---

### 📅 Day 72: Express.js Basics & First Server
- **Konsepto**: Express ang pinakasikat at pinakamagaan na web framework para sa Node.js.
  - Installing express: `npm install express`
  - `app.listen(5000, () => console.log('Server running...'))`
  - Request (`req`) at Response (`res`) objects.
- **Activity**: Gumawa ng Express server na may `/api/status` endpoint na nagbabalik ng `{ status: "online", timestamp: Date.now() }`.
- **Output**: `day-72-express-server/`

---

### 📅 Day 73: RESTful API Principles & HTTP Status Codes
- **Konsepto**: Ang standard na paraan ng pagdidisenyo ng API sa buong mundo:
  - Uniform resource naming: `/api/products` (Plural nouns, walang verbs sa URL!).
  - HTTP Verbs: `GET` (Read), `POST` (Create), `PUT`/`PATCH` (Update), `DELETE` (Remove).
  - Status Codes: `200 OK`, `201 Created`, `400 Bad Request`, `401 Unauthorized`, `404 Not Found`, `500 Server Error`.
- **Activity**: Gumawa ng API cheat sheet sa markdown na naglilista ng tamang URLs para sa isang Blog System.
- **Output**: `day-73/rest-guidelines.md`

---

### 📅 Day 74: Express Routing & Request Parameters
- **Konsepto**: Paano kumukuha ng data mula sa URL at request body?
  - Route params: `/api/products/:id` (`req.params.id`)
  - Query strings: `/api/products?search=phone&limit=10` (`req.query`)
  - Request body: `app.use(express.json())` -> (`req.body`)
- **Activity**: Gumawa ng in-memory Array CRUD API para sa `books` gamit ang iba't ibang route params.
- **Output**: `day-74-express-routes/`

---

### 📅 Day 75: Express Middleware & CORS Configuration
- **Konsepto**: Ano ang Middleware? Mga functions na tumatakbo sa pagitan ng Request at Response.
  - Custom logger middleware (nagpi-print ng method at URL).
  - Cross-Origin Resource Sharing (CORS): Bakit nagba-block ang browser kapag nag-fetch ang frontend mula sa ibang port? (`npm install cors`).
- **Activity**: I-setup ang `cors` at gumawa ng custom execution time logger middleware.
- **Output**: `day-75-middleware/`

---

### 📅 Day 76: Connecting Node.js to MySQL
- **Konsepto**: Paano kinakausap ng Express server ang MySQL database?
  - `npm install mysql2`
  - Connection Pool vs Single Connection (Bakit pool ang industry standard?).
  - `promise()` wrapper para makagamit ng `async/await`.
- **Activity**: Gumawa ng `db.js` file na nagbubukas ng connection pool sa iyong local MySQL server.
- **Output**: `day-76-mysql-connect/`

---

### 📅 Day 77: Building Full CRUD Endpoints with MySQL
- **Konsepto**: Pagsasama ng Express routes at MySQL queries:
  - `GET /api/products`: `SELECT * FROM products`
  - `GET /api/products/:id`: `SELECT * FROM products WHERE id = ?`
  - `POST /api/products`: `INSERT INTO products (name, price) VALUES (?, ?)`
  - `PUT /api/products/:id`: `UPDATE products SET name = ?, price = ? WHERE id = ?`
  - `DELETE /api/products/:id`: `DELETE FROM products WHERE id = ?`
- **Activity**: Subukan ang lahat ng 5 endpoints gamit ang **Postman** o Thunder Client!
- **Output**: `day-77-crud-api/`

---

### 📅 Day 78: MVC Pattern (Model-View-Controller)
- **Konsepto**: Huwag ilagay ang lahat ng code sa isang higanteng `index.js` file!
  - `routes/productRoutes.js` (URLs lang).
  - `controllers/productController.js` (Business logic at database queries).
  - Clean separation of concerns.
- **Activity**: I-refactor ang iyong CRUD API papuntang malinis na MVC folder structure.
- **Output**: `day-78-mvc-refactor/`

---

### 📅 Day 79: Input Validation & Sanitization
- **Konsepto**: Huwag pagkatiwalaan ang data na galing sa user!
  - `npm install zod` o `express-validator`.
  - Checking: Valid email format, password minimum length, positive prices.
  - Returning clean 400 Bad Request responses kapag may kulang o mali.
- **Activity**: Magdagdag ng Zod validation schema para sa product creation request body.
- **Output**: `day-79-validation/`

---

### 📅 Day 80: 🏆 MINI-PROJECT #8 — Products & Inventory Management REST API
- **Goal**: Isang kumpletong, professional-grade REST API na konektado sa MySQL.
- **Features**:
  1. Full CRUD para sa Products at Categories.
  2. Search at Filter query support (`/api/products?category=1&minPrice=100`).
  3. Proper HTTP Status Codes (200, 201, 400, 404, 500).
  4. Global Error Handling Middleware (hinding-hindi magka-crash ang server).
  5. Postman Collection JSON export para ma-test ng kaibigan mo.
- **Action**: I-commit sa GitHub kasama ang `schema.sql` at `postman_collection.json`.
