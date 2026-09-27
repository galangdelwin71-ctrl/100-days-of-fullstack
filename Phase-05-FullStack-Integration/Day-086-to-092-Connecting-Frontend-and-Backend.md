# 🎯 Days 86–92: Full-Stack Integration (React + Express + MySQL)

Here everything comes together. You will connect your React frontend to your Express backend and MySQL database, producing a unified Full-Stack Web Application.

---

### 📅 Day 86: Client-Server Architecture Overview
- **Concepts**: How do modern frontend and backend applications communicate?
  - Frontend runs on `http://localhost:5173` (Vite).
  - Backend runs on `http://localhost:5000` (Express).
  - Installing and setting up Axios: `npm install axios`.
  - Creating a centralized API client: `axios.create({ baseURL: 'http://localhost:5000/api' })`.
- **Activity**: Set up a project structure with `/client` and `/server` and successfully fetch data from Express into React.
- **Deliverable**: `day-86-fullstack-setup/`

---

### 📅 Day 87: Axios Client with Auth Interceptors
- **Concepts**: Eliminating manual token injection on every HTTP call:
  - Axios Request Interceptors: Automatically intercept every outgoing request, read the JWT from storage, and attach the `Authorization: Bearer <token>` header.
- **Activity**: Implement an `api.js` client module with an automated token interceptor.
- **Deliverable**: `day-87-axios-interceptors/`

---

### 📅 Day 88: React Auth Context & Persistent Sessions
- **Concepts**: Managing global authentication state across your React app:
  - React Context API (`AuthContext` and custom `useAuth()` hook).
  - States: `user`, `token`, `isAuthenticated`, `login()`, `logout()`.
  - Session hydration: Reading the stored token on initial page load to keep users logged in across browser refreshes.
- **Activity**: Build functional Login and Register pages in React that update global authentication context.
- **Deliverable**: `day-88-auth-context/`

---

### 📅 Day 89: Protected Route Guards in React
- **Concepts**: Preventing unauthorized users from accessing private routes (e.g. `/dashboard`):
  - Creating a reusable `<ProtectedRoute>` wrapper component.
  - Redirecting unauthenticated visitors to `/login`.
- **Activity**: Wrap private dashboard views inside your Protected Route component and test route protection.
- **Deliverable**: `day-89-protected-routes/`

---

### 📅 Day 90: UI Feedback: Spinners, Modals & Toast Alerts
- **Concepts**: Delivering commercial user experience:
  - Never let the interface freeze during asynchronous network operations.
  - Integrating `react-hot-toast` for alert messages ("Login successful!", "Product updated!").
  - Confirmation modals prior to destructive deletion actions.
- **Activity**: Integrate toast notifications and loading indicators across all CRUD operations.
- **Deliverable**: `day-90-ui-feedback/`

---

### 📅 Day 91: Multipart File & Image Uploads (Multer + FormData)
- **Concepts**: Handling media uploads across the stack:
  - Backend: `npm install multer` to accept and store files in an `uploads/` directory.
  - Frontend: Packaging binary files using browser `FormData`: `formData.append('image', file)`.
- **Activity**: Implement a file upload form that uploads product images or profile avatars to the server.
- **Deliverable**: `day-91-file-upload/`

---

### 📅 Day 92: Environment Variables & Secrets Management
- **Concepts**: ⚠️ Never commit database credentials or JWT secrets to GitHub!
  - Backend: `npm install dotenv` and `.env` configuration.
  - Frontend: `VITE_API_URL` configuration.
  - Maintaining `.env.example` templates for team collaborators.
- **Activity**: Sanitize all hardcoded URLs and secrets across both client and server codebases into `.env` files.
- **Deliverable**: `day-92-env-clean/`
