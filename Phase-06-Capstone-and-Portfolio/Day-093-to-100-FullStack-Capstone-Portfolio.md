# 🎯 Days 93–100: Grand Capstone Project, Cloud Deployment & Job Interview

Ito ang pinaka-highlight ng inyong 100 days! Bubuo kayo ng isang kumpletong Full-Stack Software Application na magiging bida sa inyong resume at portfolio.

---

### 💡 Pumili ng Isang Capstone Project Topic:
1. **Option A: Smart Inventory & POS/Order Tracking System** (Konektado sa business operations, sales analytics, low-stock alerts).
2. **Option B: Service Appointment & Booking Management Platform** (Schedules, customer reservations, admin approval dashboard).
3. **Option C: Mini E-Commerce Platform with Cart & Checkout Flow** (Product catalog, cart state, order placement, order history).

---

### 📅 Day 93: Capstone System Requirements & ERD Modeling
- **Task**:
  - Isulat ang listahan ng features (User Stories).
  - I-drawing ang Entity-Relationship Diagram (ERD) ng database: Users, Products/Services, Orders/Bookings, Logs.
  - I-sketch ang UI wireframes sa papel o Figma.
- **Deliverable**: `capstone/DESIGN_DOC.md` + ERD diagram image.

---

### 📅 Day 94: Capstone Database Setup & Backend Foundation
- **Task**:
  - Gumawa ng database sa MySQL gamit ang normalized tables at foreign keys.
  - Mag-initialize ng Express backend na may MVC folder structure.
  - Maglagay ng initial seed mock data para may ma-test agad.
- **Deliverable**: Gumaganang database at Express server na nag-i-initiate ng DB connection.

---

### 📅 Day 95: Capstone Authentication & API Endpoints
- **Task**:
  - I-code ang Registration at Login gamit ang bcrypt at JWT.
  - Gumawa ng full CRUD endpoints para sa pangunahing resource ng inyong app (Products, Appointments, o Orders).
  - I-test ang lahat ng endpoints sa Postman.
- **Deliverable**: Kumpletong REST API na may protected routes at Postman collection.

---

### 📅 Day 96: Capstone Frontend UI & State Architecture
- **Task**:
  - I-setup ang React Vite project na may Tailwind CSS.
  - Gumawa ng Responsive Layout: Navbar, Sidebar, Dashboard cards, Table views.
  - Ikonekta ang React AuthContext sa backend Login at Register endpoints.
- **Deliverable**: Nakakapag-login at nakakapag-register na ang user sa React frontend!

---

### 📅 Day 97: Capstone Core Business Logic & Interactivity
- **Task**:
  - I-connect ang data tables sa backend API (Fetching, Filtering, Searching).
  - Gumawa ng Add Modal / Edit Form na nagpapadala ng POST/PUT requests sa server.
  - Delete feature na may confirmation popup at toast notification.
- **Deliverable**: 100% functional CRUD flow sa UI!

---

### 📅 Day 98: Bug Hunting, UI Polish & Responsive Testing
- **Task**:
  - Subukan ang app sa cellphone screen (Inspect Element Responsive mode).
  - Ayusin ang mga overflows, sirang padding, at broken layouts.
  - Maglagay ng Loading spinners at Empty state illustrations ("No items found").
- **Deliverable**: Malinis, maganda, at walang console errors na app.

---

### 📅 Day 99: Cloud Deployment Day (Live sa Internet!)
- **Task**:
  - **Database**: Mag-spin up ng free cloud database sa Aiven, Supabase, o Railway.
  - **Backend**: I-deploy ang Express server sa **Render** o **Railway**.
  - **Frontend**: I-deploy ang React app sa **Vercel** o **Netlify**.
  - I-configure ang Environment Variables sa cloud dashboard.
- **Deliverable**: Isang **LIVE PUBLIC URL** (e.g. `https://my-capstone-app.vercel.app`) na pwede mong i-send kahit kanino!

---

### 📅 Day 100: 🎓 GRADUATION DAY — Resume, GitHub & Interview Readiness
- **Task**:
  1. **GitHub README Polish**:
     - Lagyan ng screenshots o GIF demo ng app ang inyong GitHub repository.
     - Isulat ang Tech Stack badges, Live Demo link, at Installation instructions.
  2. **I-update ang Resume**:
     - Ilagay ang Capstone Project sa ilalim ng **Projects** section ng inyong resume kasama ang live link at GitHub link.
  3. **Mock Interview kasama ang Kaibigan**:
     - Tanungin ang isa't isa:
       - *"Paano mo idinisenyo ang database schema ng app mo?"*
       - *"Bakit ka gumamit ng JWT imbes na traditional sessions?"*
       - *"Ano ang pinakamahirap na bug na na-encounter mo at paano mo ito naayos?"*
- **Deliverable**: Ready-to-apply Developer Portfolio at Resume! 🎉
