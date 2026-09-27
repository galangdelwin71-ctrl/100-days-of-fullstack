# 🎯 Days 01–10: HTML & CSS Fundamentals

During the first 10 days, you will establish the technical foundations of the modern web. Beyond syntax, you will learn to build clean, semantic, accessible, and standards-compliant web pages.

---

### 📅 Day 01: Web Architecture & Semantic HTML5
- **Concepts**: How does the web work? Client (Browser) -> DNS Resolution -> Web Server -> HTTP Response (HTML, CSS, JS). Why choose Semantic HTML (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`) over generic `<div>` soup?
- **Employer Relevance**: Semantic markup drives SEO ranking and meets legal accessibility (a11y) standards.
- **Activity**: Construct a complete personal developer bio page using proper semantic tags.
- **Deliverable**: `day-01/index.html` with valid HTML5 boilerplate and semantic layout.

---

### 📅 Day 02: HTML Forms, Input Types & Native Validation
- **Concepts**: Forms are the data-entry core of web applications (authentication, checkout, search). Master `<form>`, `<input>` variants (`text`, `email`, `password`, `number`, `tel`, `date`), `<select>`, `<textarea>`, and `<button>`. Attributes: `required`, `pattern`, `minlength`, `maxlength`, `placeholder`.
- **Activity**: Build a comprehensive User Registration Form with built-in client-side validation rules.
- **Deliverable**: `day-02/registration.html`

---

### 📅 Day 03: The CSS Box Model & Specificity Hierarchy
- **Concepts**: How does the browser calculate layout geometry?
  - **Box Model**: Margin, Border, Padding, Content.
  - The universal reset rule: `box-sizing: border-box;`.
  - Specificity calculation: Inline styles (1000) > IDs (100) > Classes/Attributes (10) > Elements (1).
- **Activity**: Code 3 distinct card components with precise padding, border treatments, and margins without causing horizontal viewport overflow.
- **Deliverable**: `day-03/box-model.html` + `day-03/style.css`

---

### 📅 Day 04: Modern Typography, Color Theory & Contrast
- **Concepts**: Elevating visual aesthetics from amateur to commercial grade:
  - Font loading via Google Fonts (Inter, Roboto, Poppins).
  - Color models: HEX, RGB, HSL.
  - WCAG Color Contrast compliance (ensuring text readability across light and dark backgrounds).
- **Activity**: Build an elegant Quote Showcase page utilizing the Inter typeface, an intentional dark color palette, and high-contrast accent highlights.
- **Deliverable**: `day-04/typography.html`

---

### 📅 Day 05: CSS Positioning Strategies (Relative, Absolute, Fixed, Sticky)
- **Concepts**: Controlling element placement within normal document flow:
  - Coordinate containment: Using `position: absolute` within a `position: relative` parent container.
  - Viewport pinning: `position: fixed` vs contextual pinning with `position: sticky`.
  - Stacking context and `z-index` layering.
- **Activity**: Build a Product Card with a floating "SALE 50% OFF" badge pinned in the top-right corner, paired with a sticky navigation header.
- **Deliverable**: `day-05/positioning.html`

---

### 📅 Day 06: CSS Flexbox Part 1 (The Flex Container)
- **Concepts**: The primary 1D layout mechanism in modern CSS:
  - `display: flex;`
  - Main Axis vs Cross Axis.
  - `flex-direction: row | column;`
  - `justify-content: flex-start | center | space-between | space-around;`
  - `align-items: stretch | center | flex-start;`
  - `gap: 1rem;`
- **Activity**: Build a standard application navigation bar (Brand Logo left, Navigation Links center, Auth CTA right) using `justify-content: space-between`.
- **Deliverable**: `day-06/flex-navbar.html`

---

### 📅 Day 07: CSS Flexbox Part 2 (The Flex Items)
- **Concepts**: How child items distribute and occupy remaining space:
  - `flex-grow`, `flex-shrink`, `flex-basis` (shorthand: `flex: 1;`).
  - Overriding alignment with `align-self`.
  - Multiline layout distribution using `flex-wrap: wrap;`.
- **Activity**: Build a responsive skill/category tag cloud that dynamically wraps across viewports without breaking container bounds.
- **Deliverable**: `day-07/flex-tags.html`

---

### 📅 Day 08: CSS Grid Part 1 (Columns & Fractional Units)
- **Concepts**: 2D layout orchestration across rows and columns simultaneously:
  - `display: grid;`
  - The fractional unit (`fr`).
  - `grid-template-columns: repeat(3, 1fr);`
  - Column and row `gap` properties.
- **Activity**: Build a structured 3-column responsive photo and media gallery.
- **Deliverable**: `day-08/grid-gallery.html`

---

### 📅 Day 09: CSS Grid Part 2 (Template Areas & Auto-Fit)
- **Concepts**: Advanced responsive Grid mechanics:
  - Semantic dashboard layouts via `grid-template-areas`.
  - Fluid responsiveness without explicit media queries: `grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));`.
- **Activity**: Construct an analytics dashboard layout featuring header, sidebar, main metric area, and footer using named grid areas.
- **Deliverable**: `day-09/grid-dashboard.html`

---

### 📅 Day 10: 🏆 MILESTONE PROJECT #1 — Responsive Developer Profile Card
- **Objective**: Synthesize HTML5 semantics, Box Model architecture, modern typography, and Flexbox/Grid layouts into a polished Developer Profile Card.
- **Feature Requirements**:
  1. Profile avatar with a live "Online" status pill indicator (`position: absolute`).
  2. Full name, bio, and social icon links (`display: flex`).
  3. Skill badges wrapped cleanly (`flex-wrap`).
  4. Metrics counter grid (Projects: 14, Reviews: 98, Rating: 4.9) structured with CSS Grid.
- **Verification**: Commit code to GitHub and share a screenshot with your study partner for review!
