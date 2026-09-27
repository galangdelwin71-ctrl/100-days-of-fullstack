# 🎯 Days 81–85: User Authentication, JWT & API Security

Dito matututunan ang pinaka-importanteng bahagi ng backend development: Paano protektahan ang user accounts at i-secure ang mga endpoints.

---

### 📅 Day 81: Password Hashing with Bcrypt
- **Konsepto**: Bakit krimen sa software engineering ang mag-save ng plain text password?
  - Salting at Hashing (One-way mathematical function).
  - `npm install bcryptjs`
  - `const salt = await bcrypt.genSalt(10);`
  - `const hash = await bcrypt.hash(password, salt);`
  - `const isMatch = await bcrypt.compare(password, hash);`
- **Activity**: Gumawa ng registration script na nagse-save ng hashed password sa database at login verifier.
- **Output**: `day-81-bcrypt/`

---

### 📅 Day 82: JWT (JSON Web Token) Anatomy & Flow
- **Konsepto**: Paano nalalaman ng server kung sino ang naka-login nang hindi gumagamit ng server memory sessions?
  - Anatomy ng Token: `Header.Payload.Signature`.
  - Stateless authentication.
  - Secret keys at token expiration (`expiresIn: '1d'`).
- **Activity**: Gumawa at mag-verify ng unang JWT gamit ang `jsonwebtoken` package: `jwt.sign()` at `jwt.verify()`.
- **Output**: `day-82-jwt-intro/`

---

### 📅 Day 83: User Registration & Login Authentication API
- **Konsepto**: Pagbuo ng complete auth workflow:
  - `POST /api/auth/register`: Check if email exists -> Hash password -> Insert to DB -> Return success.
  - `POST /api/auth/login`: Find user by email -> Compare password with bcrypt -> Generate JWT token -> Return token + user info.
- **Activity**: I-code ang Registration at Login endpoints at i-test gamit ang Postman.
- **Output**: `day-83-auth-api/`

---

### 📅 Day 84: Protected Routes & Auth Middleware
- **Konsepto**: Paano protektahan ang mga private endpoints?
  - Client sends token sa Header: `Authorization: Bearer <token>`.
  - Express Auth Middleware:
    1. Kukunin ang token mula sa `req.headers.authorization`.
    2. I-ve-verify gamit ang `jwt.verify()`.
    3. Ilalagay ang user payload sa `req.user`.
    4. Tatawagin ang `next()`. Kung invalid, magbabalik ng `401 Unauthorized`.
- **Activity**: Gumawa ng `/api/user/profile` endpoint na maa-access lang kapag may valid Bearer token.
- **Output**: `day-84-auth-middleware/`

---

### 📅 Day 85: Role-Based Access Control (Admin vs Regular User)
- **Konsepto**: Paano gumawa ng admin-only actions (hal. Delete product o view financial sales)?
  - User roles sa database: `role ENUM('user', 'admin') DEFAULT 'user'`.
  - Admin middleware: `if (req.user.role !== 'admin') return res.status(403).json({ message: "Forbidden" });`
- **Activity**: Protektahan ang `DELETE /api/products/:id` para tanging may `admin` role lang ang makapag-delete.
- **Output**: `day-85-rbac/`
