# 🎯 Days 21–30: JavaScript Logic & DOM Manipulation

Dito magsisimula ang tunay na programming logic. Gagawin nating interactive ang mga webpage sa pamamagitan ng JavaScript.

---

### 📅 Day 21: JS Variables, Data Types & Operators
- **Konsepto**: Bakit huwag nang gagamit ng `var`? (Gamitin ang `const` by default, `let` kung magbabago ang value).
  - Primitives: `string`, `number`, `boolean`, `null`, `undefined`.
  - Equality: Bakit laging `===` (strict) at iwasan ang `==` (loose)?
- **Activity**: Gumawa ng script na nagco-compute ng discount at tax para sa isang cashier system gamit ang console.
- **Output**: `day-21/basics.js`

---

### 📅 Day 22: Logic Building: If/Else, Switch & Ternary
- **Konsepto**: Conditional logic.
  - Nested conditionals vs Early return pattern (Clean code).
  - Ternary operator: `const status = isPassed ? "Approved" : "Failed";`
- **Activity**: Gumawa ng grading & scholarship evaluator function na nagre-return ng qualification message.
- **Output**: `day-22/conditions.js`

---

### 📅 Day 23: Loops & Array Fundamentals
- **Konsepto**: Arrays bilang listahan ng data.
  - Indexing (0-based).
  - `push`, `pop`, `shift`, `unshift`.
  - Loops: `for`, `for...of`, `while`.
- **Activity**: Gumawa ng inventory search loop na naghahanap ng items na out of stock (quantity <= 0).
- **Output**: `day-23/arrays.js`

---

### 📅 Day 24: Modern Array Methods (map, filter, reduce)
- **Konsepto**: Ito ang pinaka-importanteng JS concept para sa React!
  - `.map()`: Binabago ang bawat item at nagbabalik ng bagong array.
  - `.filter()`: Pini-filter ang array base sa condition.
  - `.reduce()`: Pinag-sasama ang lahat ng items (e.g., total price).
- **Activity**: May array ng 5 products (name, price, category). Gamitin ang `.filter()` para kunin ang tech items, at `.reduce()` para kunin ang kabuuang halaga.
- **Output**: `day-24/array-methods.js`

---

### 📅 Day 25: Functions, Arrow Functions & Scope
- **Konsepto**: Function declarations vs Arrow functions (`const add = (a, b) => a + b;`).
  - Global scope vs Block scope.
  - Parameters at Default values.
- **Activity**: I-convert ang 5 tradisyunal na functions papuntang malinis na arrow functions.
- **Output**: `day-25/functions.js`

---

### 📅 Day 26: Objects, Destructuring & Spread Syntax
- **Konsepto**: Paano hinahawakan ang kumplikadong data?
  - Key-value pairs.
  - Destructuring: `const { name, email } = user;`
  - Spread operator: `const updatedUser = { ...user, active: true };`
- **Activity**: Gumawa ng function na tumatanggap ng customer object at nagbabalik ng formatted shipping label gamit ang destructuring.
- **Output**: `day-26/objects.js`

---

### 📅 Day 27: DOM Selection & Content Manipulation
- **Konsepto**: Paano kinakausap ng JS ang HTML?
  - `document.querySelector()` at `document.querySelectorAll()`
  - `.textContent` vs `.innerHTML` (Bakit delikado ang innerHTML sa security?)
  - `.classList.add()`, `.classList.remove()`, `.classList.toggle()`
- **Activity**: Gumawa ng button na nag-to-toggle ng dark mode class sa `<body>`.
- **Output**: `day-27/dom-manipulation.html`

---

### 📅 Day 28: DOM Events & Event Delegation
- **Konsepto**: Pakikinig sa aksyon ng user.
  - `addEventListener('click', () => { ... })`
  - `addEventListener('submit', (e) => e.preventDefault())`
  - Event bubbling at Event delegation (pakikinig sa parent imbes na bawat child).
- **Activity**: Gumawa ng interactive counter na may `+`, `-`, at `Reset` buttons.
- **Output**: `day-28/events.html`

---

### 📅 Day 29: Browser Storage: LocalStorage & JSON
- **Konsepto**: Paano hindi mawawala ang data kahit i-refresh ang browser?
  - `localStorage.setItem('key', value)`
  - `localStorage.getItem('key')`
  - `JSON.stringify()` (Object to String) at `JSON.parse()` (String to Object).
- **Activity**: Gumawa ng note-taking app na nag-se-save ng notes sa LocalStorage.
- **Output**: `day-29/storage.html`

---

### 📅 Day 30: 🏆 MINI-PROJECT #3 — Interactive Task & Budget Tracker
- **Goal**: Full CRUD (Create, Read, Update, Delete) sa client-side gamit ang dalisay na Vanilla JavaScript.
- **Features**:
  1. Magdagdag ng Bagong Task o Expense (Title, Amount, Category).
  2. I-display sa listahan na may dynamic total computation.
  3. Mark as Complete (toggle line-through).
  4. Delete Task button na may animation.
  5. Auto-save sa `localStorage` para pag-refresh ng page ay andun pa rin ang data.
- **Review**: I-post sa GitHub repo at ipakita sa kaibigan mo!
