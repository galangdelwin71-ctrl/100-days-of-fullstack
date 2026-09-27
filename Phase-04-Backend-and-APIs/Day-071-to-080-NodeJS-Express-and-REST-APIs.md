# 🎯 Days 71–80: Node.js, Express & RESTful API Architecture

In this module, you will build production-ready backend servers that handle HTTP requests from frontend clients, run business logic, communicate with MySQL, and serve clean JSON APIs.

---

### 📅 Day 71: Node.js Architecture & Server Runtime
- **Concepts**: What is Node.js? Executing JavaScript outside the browser:
  - V8 engine and libuv asynchronous I/O.
  - Native core modules: `fs`, `path`, `http`.
  - Module formats: CommonJS (`require`) vs ES Modules (`import/export`).
- **Activity**: Build a Node CLI script that reads a JSON file from disk, modifies its values, and writes it back asynchronously.
- **Deliverable**: `day-71-node/index.js`

---

### 📅 Day 72: Express.js Framework & Server Setup
- **Concepts**: Express is the minimalist, industry-standard web framework for Node.js:
  - `npm install express`.
  - Server listener: `app.listen(5000, () => console.log('Server running...'))`.
  - Request (`req`) and Response (`res`) objects.
- **Activity**: Launch an Express server exposing a health check endpoint: `GET /api/health` returning `{ status: "ok", uptime: process.uptime() }`.
- **Deliverable**: `day-72-express-server/`

---

### 📅 Day 73: RESTful API Principles & HTTP Status Codes
- **Concepts**: Industry design standards for predictable APIs:
  - Resource-oriented URLs: `/api/products` (Plural nouns, verbs belong in HTTP methods!).
  - Standard HTTP verbs: `GET` (Read), `POST` (Create), `PUT`/`PATCH` (Update), `DELETE` (Remove).
  - Accurate HTTP status codes: `200 OK`, `201 Created`, `400 Bad Request`, `401 Unauthorized`, `404 Not Found`, `500 Internal Server Error`.
- **Activity**: Author a comprehensive API specification document for a Blog engine adhering strictly to REST conventions.
- **Deliverable**: `day-73/rest-guidelines.md`

---

### 📅 Day 74: Express Routing & Request Parameters
- **Concepts**: Extracting data from incoming client requests:
  - URL route parameters: `/api/products/:id` accessed via `req.params.id`.
  - Query parameters: `/api/products?search=shoes&limit=5` accessed via `req.query`.
  - JSON body parsing: `app.use(express.json())` and reading `req.body`.
- **Activity**: Construct in-memory CRUD routes for a `books` collection supporting ID lookups and search filtering.
- **Deliverable**: `day-74-express-routes/`

---

### 📅 Day 75: Express Middleware Pipeline & CORS Policies
- **Concepts**: The middleware processing pipeline:
  - Request -> Middleware 1 -> Middleware 2 -> Controller -> Response.
  - Custom request logging middleware.
  - Cross-Origin Resource Sharing (CORS): Configuring the `cors` package so frontend apps can safely call the API.
- **Activity**: Configure CORS and write a custom middleware logging HTTP method, request path, and execution duration in milliseconds.
- **Deliverable**: `day-75-middleware/`

---

### 📅 Day 76: Connecting Node.js to MySQL via Connection Pools
- **Concepts**: Enterprise database communication:
  - `npm install mysql2`.
  - Single Connection vs Connection Pooling (Why pooling is mandatory for concurrency).
  - Leveraging the `promise()` wrapper for seamless `async/await` queries.
- **Activity**: Create a reusable `db.js` database utility module exporting an active MySQL connection pool.
- **Deliverable**: `day-76-mysql-connect/`

---

### 📅 Day 77: Full CRUD REST Endpoints with MySQL
- **Concepts**: Integrating Express route handlers with live SQL queries:
  - `GET /api/products`: `SELECT * FROM products`
  - `GET /api/products/:id`: `SELECT * FROM products WHERE id = ?`
  - `POST /api/products`: `INSERT INTO products (name, price) VALUES (?, ?)`
  - `PUT /api/products/:id`: `UPDATE products SET name = ?, price = ? WHERE id = ?`
  - `DELETE /api/products/:id`: `DELETE FROM products WHERE id = ?`
- **Activity**: Test all 5 CRUD operations against your local MySQL database using **Postman**.
- **Deliverable**: `day-77-crud-api/`

---

### 📅 Day 78: The MVC Architecture (Model-View-Controller)
- **Concepts**: Enterprise code organization:
  - Eliminating bloated single-file servers.
  - `routes/productRoutes.js`: Clean endpoint definitions.
  - `controllers/productController.js`: Business logic, validation, and database operations.
- **Activity**: Refactor your monolithic CRUD server into structured MVC layers.
- **Deliverable**: `day-78-mvc-refactor/`

---

### 📅 Day 79: Request Validation & Sanitization (Zod / Joi)
- **Concepts**: The golden rule of backend development: **Never trust client input!**
  - Using schema validation libraries like `zod`.
  - Enforcing strict requirements: Valid email syntax, password minimums, non-negative numbers.
  - Halting invalid requests with structured `400 Bad Request` validation error payloads.
- **Activity**: Create a Zod validation middleware that checks incoming product creation bodies before reaching the controller.
- **Deliverable**: `day-79-validation/`

---

### 📅 Day 80: 🏆 MILESTONE PROJECT #8 — Products & Categories REST API
- **Objective**: Deliver a production-grade, architecturally sound REST API connected to MySQL.
- **Feature Requirements**:
  1. Full CRUD operations across Products and Categories.
  2. Query support for searching, category filtering, and price limits.
  3. Consistent HTTP status codes and uniform JSON response envelopes.
  4. Global error-handling middleware preventing unhandled exceptions from crashing the process.
  5. Exported Postman Collection JSON file for peer testing.
- **Verification**: Commit the backend project along with the Postman collection to GitHub!
