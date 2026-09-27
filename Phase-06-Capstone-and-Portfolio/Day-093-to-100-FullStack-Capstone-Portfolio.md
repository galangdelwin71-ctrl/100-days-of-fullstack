# 🎯 Days 93–100: Grand Capstone Project, Cloud Deployment & Job Readiness

This is the culmination of your 100-day journey. You will build, polish, and deploy an end-to-end Full-Stack Application that will serve as the flagship project of your resume and portfolio.

---

### 💡 Choose One Capstone Concept:
1. **Option A: Smart Inventory & POS/Order Tracking System** (Product catalogs, sales analytics, stock thresholds, receipt printing).
2. **Option B: Service Appointment & Booking Management Platform** (Schedules, customer reservations, admin approval workflows, email alerts).
3. **Option C: Multi-Vendor E-Commerce Platform with Cart & Checkout Flow** (Catalogs, cart state, order placement, customer order history).

---

### 📅 Day 93: Capstone System Requirements & ERD Modeling
- **Tasks**:
  - Author a User Story specification outlining MVP requirements.
  - Draw the complete Entity-Relationship Diagram (ERD): Users, Products/Services, Orders/Bookings, Logs.
  - Sketch wireframes in Figma or on paper.
- **Deliverable**: `capstone/DESIGN_DOC.md` and ERD model image.

---

### 📅 Day 94: Capstone Database Setup & Backend Foundation
- **Tasks**:
  - Initialize the MySQL database with normalized tables, constraints, and indexes.
  - Scaffold the Express backend using the MVC architecture.
  - Seed initial mock data for immediate testing.
- **Deliverable**: Operational database and Express server connected via connection pooling.

---

### 📅 Day 95: Capstone Authentication & API Endpoints
- **Tasks**:
  - Implement registration, login, password hashing, and JWT generation.
  - Build full CRUD endpoints for the core domain resource (Products, Appointments, or Orders).
  - Verify every endpoint using Postman.
- **Deliverable**: Fully functioning, protected REST API with an exported Postman collection.

---

### 📅 Day 96: Capstone Frontend UI & State Architecture
- **Tasks**:
  - Initialize the React + Vite frontend styled with Tailwind CSS.
  - Build responsive layouts: Navigation, Sidebar, Dashboard cards, and Data Tables.
  - Connect React AuthContext with the backend login/registration endpoints.
- **Deliverable**: Fully functional authentication flow on the React frontend.

---

### 📅 Day 97: Capstone Core Business Logic & Interactivity
- **Tasks**:
  - Connect frontend tables to backend APIs (Fetching, Filtering, Searching, Pagination).
  - Implement Add/Edit modal dialogs with form validation.
  - Implement deletion actions with confirmation modals and toast alerts.
- **Deliverable**: 100% complete end-to-end CRUD workflow functioning smoothly in the browser.

---

### 📅 Day 98: Bug Hunting, UI Polish & Responsive Audit
- **Tasks**:
  - Test the application on mobile device viewports.
  - Resolve layout overflows, misaligned items, and contrast issues.
  - Add loading skeleton animations and empty-state placeholders.
- **Deliverable**: A polished, error-free web application ready for public demonstration.

---

### 📅 Day 99: Cloud Deployment Day (Live on the Internet!)
- **Tasks**:
  - **Database**: Provision a managed cloud database instance (Aiven, Supabase, or Railway).
  - **Backend**: Deploy the Express server to **Render** or **Railway**.
  - **Frontend**: Deploy the React app to **Vercel** or **Netlify**.
  - Configure cloud environment variables (`DATABASE_URL`, `JWT_SECRET`, `VITE_API_URL`).
- **Deliverable**: A **LIVE PUBLIC HTTPS URL** you can share with employers and colleagues worldwide!

---

### 📅 Day 100: 🎓 GRADUATION DAY — Portfolio, Resume & Interview Mastery
- **Tasks**:
  1. **GitHub README Polish**:
     - Embed high-resolution application screenshots and demo GIFs into your repository README.
     - Document tech stack badges, live demo link, and local installation steps.
  2. **Update Your Resume**:
     - Feature this Capstone Project prominently in the **Projects** section of your resume with its live link and GitHub repository.
  3. **Mock Technical Interview with Your Study Partner**:
     - Take turns grilling each other on engineering decisions:
       - *"How did you design your database schema to prevent data anomalies?"*
       - *"Why did you choose JWT over stateful server sessions?"*
       - *"What was the most challenging bug you encountered and how did you resolve it?"*
- **Deliverable**: A production-ready developer portfolio and technical interview confidence! 🎉
