# 🎯 Days 11–20: Responsive Design, UI/UX & Modern CSS

Sa bahaging ito, gagawin mong mobile-friendly ang iyong mga website, matututunan ang micro-interactions, at magdidisenyo na parang professional UI/UX designer.

---

### 📅 Day 11: Mobile-First Responsive Design & Media Queries
- **Konsepto**: Bakit mobile-first? Higit 60% ng web traffic ay nasa cellphone.
  - `@media (min-width: 640px) { ... }` (Tablet)
  - `@media (min-width: 1024px) { ... }` (Desktop)
- **Activity**: I-convert ang isang 1-column mobile layout papuntang 3-column desktop layout gamit ang media queries.
- **Output**: `day-11/responsive-card.html`

---

### 📅 Day 12: CSS Variables & Dark Mode Toggle
- **Konsepto**: CSS Custom Properties (`:root { --bg-color: #ffffff; --text-color: #111827; }`).
  - Dark mode styles: `[data-theme="dark"] { --bg-color: #0f172a; --text-color: #f8fafc; }`.
- **Activity**: Gumawa ng page na nagpapalit ng colors sa pamamagitan lang ng CSS variables.
- **Output**: `day-12/dark-mode-preview.html`

---

### 📅 Day 13: CSS Transitions, Transforms & Hover Effects
- **Konsepto**: Micro-animations na nagbibigay-buhay sa website.
  - `transition: all 0.3s ease-in-out;`
  - `transform: translateY(-4px) scale(1.02);`
  - Box-shadow elevations sa hover.
- **Activity**: Mag-design ng 3 interactive action buttons (Primary, Outline, Gradient glow) na may smooth hover animation.
- **Output**: `day-13/micro-interactions.html`

---

### 📅 Day 14: CSS Keyframe Animations & Loading Spinners
- **Konsepto**: Custom animations gamit ang `@keyframes`.
  - Pulse effects, skeleton loaders, at rotating spinners.
- **Activity**: Gumawa ng modern loading spinner at isang shimmering skeleton card loader.
- **Output**: `day-14/loaders.html`

---

### 📅 Day 15: Introduction to Tailwind CSS
- **Konsepto**: Bakit karamihan ng modern tech companies ay gumagamit ng Tailwind CSS? Utility classes (`flex`, `items-center`, `p-4`, `rounded-xl`, `bg-blue-600`).
- **Activity**: Gumawa ng alert box at modal popup gamit ang Tailwind Play (o CDN).
- **Output**: `day-15/tailwind-intro.html`

---

### 📅 Day 16: UI/UX Principles for Developers
- **Konsepto**: Hindi mo kailangang maging artist para makagawa ng magandang UI!
  - 4 Core Rules: **Contrast**, **Repetition**, **Alignment**, **Proximity** (CRAP principle).
  - Whitespace: Huwag siksikin ang mga elemento.
- **Activity**: Kumuha ng isang pangit/makalat na form at i-redesign ito gamit ang proper spacing at visual hierarchy.
- **Output**: `day-16/before-after-ui.html`

---

### 📅 Day 17: Figma to Code: Translating Designs
- **Konsepto**: Paano nagtutulungan ang UI Designer at Web Developer?
  - Pagkuha ng CSS values (font-size, hex colors, padding) mula sa Figma inspection panel.
- **Activity**: Buksan ang isang libreng Figma community template (hal. Mobile Card) at i-code ito nang eksaktong-eksakto (pixel-perfect).
- **Output**: `day-17/figma-clone.html`

---

### 📅 Day 18: Responsive Navigation Bar with Mobile Drawer
- **Konsepto**: Ang pinaka-karaniwang interview exam component: Responsive Navbar.
  - Desktop: Horizontal links.
  - Mobile: Hamburger button na nagbubukas ng slide-in menu drawer.
- **Activity**: I-code ang responsive navbar gamit ang HTML at CSS (checkbox hack o basic JS toggle).
- **Output**: `day-18/responsive-nav.html`

---

### 📅 Day 19: Pricing Table with Feature Comparison
- **Konsepto**: Modern card design na may "Most Popular" highlight badge, list of checkmarked features, at call-to-action button.
- **Activity**: Gumawa ng 3-tier pricing table (Starter, Pro, Enterprise) na responsive sa mobile at desktop.
- **Output**: `day-19/pricing-table.html`

---

### 📅 Day 20: 🏆 MINI-PROJECT #2 — Modern Business Landing Page
- **Goal**: Isang complete, responsive landing page para sa isang startup o local business (hal. Coffee Shop o Tech Agency).
- **Sections**:
  1. Sticky Navigation na may logo at CTA.
  2. Hero Section na may headline, subtext, at CTA button.
  3. Features Grid (3 o 4 cards).
  4. Pricing Table.
  5. Footer na may social links at copyright.
- **Review**: I-deploy sa **GitHub Pages** para ma-view ng kaibigan mo sa phone nila!
