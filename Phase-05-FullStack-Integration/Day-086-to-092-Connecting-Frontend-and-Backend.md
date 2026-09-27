# 🎯 Days 86–92: Full-Stack Integration (React + Express + MySQL)

Dito pagtatagpuin ang lahat ng inyong natutunan! Ikokonekta ninyo ang React Frontend sa Express Backend at MySQL Database para maging isang buong Full-Stack Application.

---

### 📅 Day 86: Client-Server Architecture Overview
- **Konsepto**: Paano nag-uusap ang Frontend at Backend sa totoong mundo?
  - Frontend tumatakbo sa `http://localhost:5173` (Vite).
  - Backend tumatakbo sa `http://localhost:5000` (Express).
  - Axios HTTP client setup (`npm install axios`).
  - Base URL configuration (`axios.create({ baseURL: 'http://localhost:5000/api' })`).
- **Activity**: Mag-setup ng monorepo o dalawang magkatabing folders (`/client` at `/server`) at subukang mag-fetch ng data mula sa React papuntang Express.
- **Output**: `day-86-fullstack-setup/`

---

### 📅 Day 87: Axios Client with Auth Interceptors
- **Konsepto**: Paano hindi mano-manong ilalagay ang Bearer token sa bawat API call?
  - Axios Request Interceptor: Kusa nitong kukunin ang token mula sa LocalStorage at ididikit sa `Authorization` header bago lumipad ang request.
- **Activity**: I-code ang reusable `api.js` Axios instance na may token interceptor.
- **Output**: `day-87-axios-interceptors/`

---

### 📅 Day 88: Auth Context & Persistent Login State in React
- **Konsepto**: Global state para sa authentication:
  - React Context API (`AuthContext` at `useAuth()` custom hook).
  - State: `user`, `token`, `isAuthenticated`, `login()`, `logout()`.
  - Pag-refresh ng page: Kusa nitong babasahin ang token sa LocalStorage para hindi ma-logout ang user.
- **Activity**: Gumawa ng Login at Register pages sa React na konektado sa backend.
- **Output**: `day-88-auth-context/`

---

### 📅 Day 89: Protected Route Guards in React
- **Konsepto**: Paano pigilan ang mga hindi naka-login na pumunta sa `/dashboard`?
  - `<ProtectedRoute>` wrapper component.
  - Redirect papuntang `/login` kapag walang active session.
- **Activity**: I-wrap ang Dashboard view sa Protected Route component.
- **Output**: `day-89-protected-routes/`

---

### 📅 Day 90: UI Loading States, Modals & Toast Notifications
- **Konsepto**: Professional user feedback.
  - Huwag i-freeze ang UI habang naghihintay ng server response.
  - `react-hot-toast` para sa mga mensahe ("Login successful!", "Product added!").
  - Confirmation modals bago mag-delete.
- **Activity**: Mag-install ng `react-hot-toast` at magpakita ng toast notifications sa bawat CRUD action.
- **Output**: `day-90-ui-feedback/`

---

### 📅 Day 91: Handling Image & File Uploads (Multer)
- **Konsepto**: Paano mag-upload ng product pictures o user avatars?
  - Backend: `npm install multer` para mag-save ng files sa `uploads/` folder.
  - Frontend: `FormData` API (`const formData = new FormData(); formData.append('image', file);`).
- **Activity**: Gumawa ng image upload feature para sa isang profile picture o product item.
- **Output**: `day-91-file-upload/`

---

### 📅 Day 92: Environment Variables (`.env`) & Secrets Security
- **Konsepto**: ⚠️ Huwag i-commit ang database passwords at JWT secrets sa GitHub!
  - `npm install dotenv`
  - `.env` file (ilagay sa `.gitignore`).
  - `.env.example` file (template na walang totoong passwords para sa kaibigan mo).
  - Frontend env: `VITE_API_URL`.
- **Activity**: I-linis ang lahat ng hardcoded URLs at secrets gamit ang `.env` files sa client at server.
- **Output**: `day-92-env-clean/`
