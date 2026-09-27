# 🎯 Days 01–10: HTML & CSS Fundamentals

Sa unang 10 araw, itatayo ninyo ang pundasyon ng modernong web. Hindi lang basta tag at kulay — matututunan ninyo kung paano gumawa ng malinis, semantic, at accessible na webpage.

---

### 📅 Day 01: Web Anatomy & Semantic HTML5
- **Konsepto**: Paano gumagana ang web? Browser -> DNS -> Server -> Response (HTML/CSS/JS). Bakit mahalaga ang Semantic HTML (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`) kaysa puro `<div>`?
- **Bakit Gusto ng Company**: SEO-friendly at accessible para sa screen readers.
- **Activity**: Gumawa ng semantic structure ng isang personal bio page. Gamitin lahat ng nabanggit na semantic tags.
- **Output**: `day-01/index.html` na may valid HTML5 boilerplate at semantic structure.

---

### 📅 Day 02: HTML Forms, Inputs & Client Validation
- **Konsepto**: Forms ang puso ng web apps (login, sign up, checkout). Pag-aralan ang `<form>`, `<input>` types (`text`, `email`, `password`, `number`, `date`), `<select>`, `<textarea>`, `<button>`. Attributes: `required`, `pattern`, `minlength`, `placeholder`.
- **Activity**: Gumawa ng User Registration Form na may kumpletong validation (Name, Email, Password, Birthdate, Role selector, Terms checkbox).
- **Output**: `day-02/registration.html`

---

### 📅 Day 03: CSS Basics, Box Model & Specificity
- **Konsepto**: Paano kino-compute ng browser ang itsura ng elements? 
  - **Box Model**: Margin, Border, Padding, Content.
  - `box-sizing: border-box;` (Bakit ito ang golden rule sa modern CSS?)
  - CSS Specificity: Inline > ID > Class > Element.
- **Activity**: Mag-style ng 3 magkakaibang cards. I-set ang padding, margin, at borders nang hindi lumalampas sa screen.
- **Output**: `day-03/box-model.html` + `day-03/style.css`

---

### 📅 Day 04: Typography, Modern Colors & Contrast
- **Konsepto**: Bakit pangit tingnan ang default browser fonts?
  - Google Fonts (Inter, Outfit, Poppins).
  - Modern Color Systems (HEX, RGB, HSL).
  - Accessibility: WCAG Color Contrast (madaling basahin, hindi masakit sa mata).
- **Activity**: Gumawa ng isang Quote Showcase page gamit ang Inter font, magandang dark background, at accent color.
- **Output**: `day-04/typography.html`

---

### 📅 Day 05: CSS Positioning (Static, Relative, Absolute, Fixed, Sticky)
- **Konsepto**: Kailan ginagamit ang `position: absolute` sa loob ng `position: relative`? Paano gumawa ng sticky navbar o floating badge?
- **Activity**: Gumawa ng product card na may floating "SALE 50% OFF" badge sa upper-right corner, at isang sticky navigation bar.
- **Output**: `day-05/positioning.html`

---

### 📅 Day 06: CSS Flexbox Part 1 (The Container)
- **Konsepto**: Flexbox ang pinaka-ginagamit na layout tool sa frontend.
  - `display: flex;`
  - `flex-direction: row | column;`
  - `justify-content: flex-start | center | space-between | space-around;`
  - `align-items: stretch | center | flex-start;`
  - `gap: 1rem;`
- **Activity**: Gumawa ng standard web navigation header (Logo sa kaliwa, Nav Links sa gitna, Login Button sa kanan) gamit ang `justify-content: space-between`.
- **Output**: `day-06/flex-navbar.html`

---

### 📅 Day 07: CSS Flexbox Part 2 (The Items)
- **Konsepto**: Paano nag-aadjust ang mga anak na element?
  - `flex-grow`, `flex-shrink`, `flex-basis` (shorthand: `flex: 1;`).
  - `align-self` (overriding container alignment).
  - `flex-wrap: wrap;` (para bumaba kapag masikip).
- **Activity**: Gumawa ng responsive tags/badges cloud na nag-w-wrap kapag pinaliit ang browser.
- **Output**: `day-07/flex-tags.html`

---

### 📅 Day 08: CSS Grid Part 1 (Columns & Rows)
- **Konsepto**: Kailan gagamit ng Grid imbes na Flexbox? (Grid = 2D layouts: rows & columns sabay; Flexbox = 1D: row o column lang).
  - `display: grid;`
  - `grid-template-columns: repeat(3, 1fr);`
  - `gap: 1.5rem;`
- **Activity**: Gumawa ng 3-column photo gallery layout.
- **Output**: `day-08/grid-gallery.html`

---

### 📅 Day 09: CSS Grid Part 2 (Template Areas & Auto-Fit)
- **Konsepto**: 
  - `grid-template-areas` para sa dashboard layout (header, sidebar, main, footer).
  - Responsive without media queries: `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));`
- **Activity**: Gumawa ng responsive dashboard layout gamit ang `grid-template-areas`.
- **Output**: `day-09/grid-dashboard.html`

---

### 📅 Day 10: 🏆 MINI-PROJECT #1 — Responsive Developer Profile Card
- **Goal**: Pagsamahin ang HTML5, Box Model, Typography, at Flexbox/Grid para gumawa ng isang modernong Profile Card.
- **Features**:
  - Profile avatar na may active status indicator badge (position absolute).
  - Pangalan, Bio, Social media links (Flexbox row).
  - Skills chips / tags (`flex-wrap`).
  - Stats counter (Projects: 12, Followers: 1.4k, Rating: 5.0) gamit ang Grid.
- **Action**: I-commit sa GitHub at i-share ang screenshot sa kaibigan mo!
