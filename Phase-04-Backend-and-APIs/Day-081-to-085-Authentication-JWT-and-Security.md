# 🎯 Days 81–85: User Authentication, JWT & Security

In this module, you will master the most critical layer of backend engineering: Securing user accounts, managing cryptographic sessions, and safeguarding protected routes.

---

### 📅 Day 81: Password Cryptography with Bcrypt
- **Concepts**: Why storing plain-text passwords is an unforgivable security breach:
  - Cryptographic Salt and One-Way Hashing algorithms.
  - `npm install bcryptjs`.
  - `const salt = await bcrypt.genSalt(10);`.
  - `const hash = await bcrypt.hash(plainPassword, salt);`.
  - `const isMatch = await bcrypt.compare(candidatePassword, hash);`.
- **Activity**: Implement a registration script that saves hashed passwords to MySQL and verifies login attempts securely.
- **Deliverable**: `day-81-bcrypt/`

---

### 📅 Day 82: JWT (JSON Web Token) Architecture
- **Concepts**: Modern stateless authentication:
  - Token anatomy: `Header.Payload.Signature`.
  - Session cookies vs Stateless Bearer Tokens.
  - Secret keys and expiration lifespans (`expiresIn: '1d'`).
- **Activity**: Generate and verify JWT tokens using the `jsonwebtoken` package: `jwt.sign()` and `jwt.verify()`.
- **Deliverable**: `day-82-jwt-intro/`

---

### 📅 Day 83: User Registration & Login Authentication Pipeline
- **Concepts**: End-to-end authentication workflow:
  - `POST /api/auth/register`: Validate email availability -> Hash password -> Insert to MySQL -> Return success.
  - `POST /api/auth/login`: Locate user by email -> Verify password with bcrypt -> Generate signed JWT -> Return token and user metadata.
- **Activity**: Build both endpoints and verify them across valid and invalid credentials in Postman.
- **Deliverable**: `day-83-auth-api/`

---

### 📅 Day 84: Protected Routes & Auth Middleware
- **Concepts**: Safeguarding private endpoints:
  - Clients pass credentials in the request header: `Authorization: Bearer <token>`.
  - Authentication Middleware logic:
    1. Extract Bearer token from `req.headers.authorization`.
    2. Verify signature using `jwt.verify()`.
    3. Attach authenticated user payload to `req.user`.
    4. Call `next()`, or reject with `401 Unauthorized` on failure.
- **Activity**: Build a protected `GET /api/user/profile` endpoint accessible only with a valid Bearer token.
- **Deliverable**: `day-84-auth-middleware/`

---

### 📅 Day 85: Role-Based Access Control (RBAC: Admin vs User)
- **Concepts**: Restricting sensitive operations based on permissions:
  - Database schema: `role ENUM('user', 'admin') DEFAULT 'user'`.
  - Authorization middleware: `if (req.user.role !== 'admin') return res.status(403).json({ message: "Forbidden" });`.
- **Activity**: Protect administrative endpoints (e.g. `DELETE /api/products/:id`) so only users with an `admin` role can execute them.
- **Deliverable**: `day-85-rbac/`
