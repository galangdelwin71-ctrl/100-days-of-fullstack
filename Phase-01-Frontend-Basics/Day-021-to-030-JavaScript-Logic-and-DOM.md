# 🎯 Days 21–30: JavaScript Logic & DOM Manipulation

Here begins core programming logic. You will transform static web layouts into dynamic, interactive web applications using modern JavaScript.

---

### 📅 Day 21: Variables, Data Types & Equality Operators
- **Concepts**: Why modern JavaScript avoids `var`:
  - `const` by default for immutable bindings; `let` when reassignment is mandatory.
  - Primitive types: `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.
  - Strict equality (`===`) vs Loose equality (`==`) and type coercion pitfalls.
- **Activity**: Build a console utility script that calculates tax, discounts, and final checkout prices for an e-commerce cashier engine.
- **Deliverable**: `day-21/basics.js`

---

### 📅 Day 22: Conditional Logic, Guard Clauses & Ternary Operators
- **Concepts**: Structuring decision branches cleanly:
  - Avoiding deeply nested `if/else` ladders using early return / guard clauses.
  - The ternary operator: `const status = isVerified ? "Active" : "Pending";`.
  - Logical short-circuiting: `const user = profile || defaultProfile;`.
- **Activity**: Build an applicant qualification evaluator function that evaluates test scores, age, and prerequisites using guard clauses.
- **Deliverable**: `day-22/conditions.js`

---

### 📅 Day 23: Loops & Array Fundamentals
- **Concepts**: Managing ordered collections of data:
  - 0-based array indexing.
  - Mutation methods: `push()`, `pop()`, `shift()`, `unshift()`.
  - Iteration: `for`, `for...of`, and `while` loops.
- **Activity**: Write an inventory audit loop that scans an array of stock items and identifies products needing restocking (quantity <= 5).
- **Deliverable**: `day-23/arrays.js`

---

### 📅 Day 24: Functional Array Methods (map, filter, reduce)
- **Concepts**: The most crucial JavaScript array methods for React development:
  - `.map()`: Transforms each element into a new array.
  - `.filter()`: Returns a subset matching a boolean condition.
  - `.reduce()`: Accumulates array elements into a single aggregate value.
  - `.find()` and `.some()`.
- **Activity**: Given an array of 6 product objects, use `.filter()` to extract electronics and `.reduce()` to compute total inventory value.
- **Deliverable**: `day-24/array-methods.js`

---

### 📅 Day 25: Functions, Arrow Syntax, Scope & Closures
- **Concepts**: Modularizing reusable logic:
  - Function declarations vs concise Arrow Functions (`const add = (a, b) => a + b;`).
  - Block scope vs Function scope.
  - Lexical scope and Closures: Functions remembering their outer variable environment.
- **Activity**: Refactor 5 traditional functions into arrow functions and implement a counter generator using a closure.
- **Deliverable**: `day-25/functions.js`

---

### 📅 Day 26: Objects, Destructuring & Spread/Rest Syntax
- **Concepts**: Managing structured key-value entities:
  - Object literals and property access.
  - Object & Array destructuring: `const { name, role } = employee;`.
  - Spread operator (`...`) for immutable object cloning and property overrides.
- **Activity**: Build an order processor function that accepts customer details and cart items, merging them into a formatted invoice object.
- **Deliverable**: `day-26/objects.js`

---

### 📅 Day 27: DOM Traversal, Querying & Manipulation
- **Concepts**: How JavaScript interacts with the live document tree:
  - `document.querySelector()` and `document.querySelectorAll()`.
  - Safe text updates: `.textContent` vs the security risks of `.innerHTML` (XSS vulnerability).
  - Class management: `.classList.add()`, `.classList.remove()`, `.classList.toggle()`.
- **Activity**: Create a dark mode toggle button that dynamically adds and removes CSS classes on the `<body>` element.
- **Deliverable**: `day-27/dom-manipulation.html`

---

### 📅 Day 28: DOM Events & Event Delegation
- **Concepts**: Responding to user interactions:
  - `addEventListener('click', handler)`.
  - Form interception: `event.preventDefault()`.
  - Event propagation: Event Bubbling and Event Delegation (attaching a single listener to a parent list instead of dozens of children).
- **Activity**: Build an interactive counter widget with increment, decrement, and reset actions handled via event delegation.
- **Deliverable**: `day-28/events.html`

---

### 📅 Day 29: Browser Storage: LocalStorage & JSON Serialization
- **Concepts**: Persisting application state across page reloads:
  - Key-value storage: `localStorage.setItem(key, value)` and `localStorage.getItem(key)`.
  - Data serialization: `JSON.stringify()` (Object -> String) and `JSON.parse()` (String -> Object).
- **Activity**: Build a persistent quick-notes scratchpad that automatically saves notes to LocalStorage on input.
- **Deliverable**: `day-29/storage.html`

---

### 📅 Day 30: 🏆 MILESTONE PROJECT #3 — Interactive Task & Budget Manager
- **Objective**: Build a complete client-side CRUD (Create, Read, Update, Delete) application using pure Vanilla JavaScript.
- **Feature Requirements**:
  1. Add new items with title, amount, category, and date.
  2. Display active records in a clean table with dynamic total computation.
  3. Mark items as completed / paid with toggleable UI styling.
  4. Delete items with smooth DOM removal animation.
  5. Automatic synchronization with `localStorage` so data survives browser refresh.
- **Verification**: Commit code to your GitHub repo and review your partner's code structure!
