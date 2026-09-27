# 🎯 Days 31–40: Modern JavaScript, Async/Await & APIs

In this phase, you will learn to connect applications to real-world cloud APIs using asynchronous JavaScript and adopt industry-standard tooling like Vite and Git.

---

### 📅 Day 31: Asynchronous Architecture & The Event Loop
- **Concepts**: How does JavaScript execute non-blocking operations despite being single-threaded?
  - Call Stack, Web APIs, Microtask Queue, Task/Callback Queue, and the Event Loop.
  - Timers: `setTimeout()` and `setInterval()`.
- **Activity**: Construct an accurate digital stopwatch application with start, pause, and reset controls using `setInterval()`.
- **Deliverable**: `day-31/clock.html`

---

### 📅 Day 32: JavaScript Promises & Error Propagation
- **Concepts**: Escaping "Callback Hell":
  - Promise lifecycles: `Pending`, `Fulfilled`, `Rejected`.
  - Method chaining with `.then()`, `.catch()`, and `.finally()`.
- **Activity**: Implement a simulated asynchronous payment verification promise that resolves on success and rejects on network timeout.
- **Deliverable**: `day-32/promises.js`

---

### 📅 Day 33: Async / Await Syntax & Try/Catch Patterns
- **Concepts**: The modern, readable standard for handling asynchronous code:
  - Declaring `async` functions and consuming promises with `await`.
  - Robust exception handling via structured `try { ... } catch (error) { ... }` blocks.
- **Activity**: Refactor your Day 32 Promise code into clean `async/await` functions with comprehensive error trapping.
- **Deliverable**: `day-33/async-await.js`

---

### 📅 Day 34: Fetch API: Consuming Public REST Endpoints
- **Concepts**: Retrieving live remote data over HTTP:
  - Calling `fetch('https://api.example.com/data')`.
  - Parsing payloads: `const data = await response.json();`.
  - Checking `response.ok` before reading data.
- **Activity**: Fetch live quotes or dummy posts from [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts) and render them into cards.
- **Deliverable**: `day-34/fetch-quotes.html`

---

### 📅 Day 35: Fetch API: Mutations (POST, PUT, DELETE)
- **Concepts**: Sending data back to external servers:
  - Setting HTTP methods (`POST`, `PUT`, `DELETE`).
  - Specifying request headers (`'Content-Type': 'application/json'`).
  - Serializing request bodies: `JSON.stringify(payload)`.
- **Activity**: Build a form interface that dispatches a simulated POST request payload to JSONPlaceholder.
- **Deliverable**: `day-35/fetch-post.html`

---

### 📅 Day 36: Handling API States: Loading, Error & Empty
- **Concepts**: The hallmark of professional engineering:
  - Never leave a blank or unresponsive screen during network activity.
  - Display loading skeleton / spinner state while awaiting response.
  - Render user-friendly error banners on HTTP failures (404, 500) and empty-state placeholders when results array is empty.
- **Activity**: Build a resilient data search view that gracefully handles all 3 states (Loading, Error, Empty).
- **Deliverable**: `day-36/api-states.html`

---

### 📅 Day 37: Modern Developer Tooling: Node.js, NPM & Vite
- **Concepts**: Why modern projects rely on build bundlers:
  - Package management: `package.json`, `npm install`, dependencies vs devDependencies.
  - Vite: The lightning-fast frontend development server and bundler.
- **Activity**: Initialize your first Vite application via the terminal: `npm create vite@latest my-app -- --template vanilla`.
- **Deliverable**: Verify the local dev server runs cleanly at `http://localhost:5173`.

---

### 📅 Day 38: Professional Git Team Workflow: Branches & Pull Requests
- **Concepts**: How engineering teams collaborate on a shared codebase:
  - Branching: `git checkout -b feature/search-bar`.
  - Pushing branches: `git push origin feature/search-bar`.
  - Opening a Pull Request (PR) on GitHub, requesting peer reviews, and merging.
- **Activity**: Pair up with your partner. Partner 1 creates a PR for a Navbar feature; Partner 2 reviews and approves the merge.
- **Deliverable**: A successfully merged Pull Request visible on your repository's GitHub history.

---

### 📅 Day 39: Chrome DevTools: Network Tab & Performance Debugging
- **Concepts**: The engineer's essential diagnostics suite:
  - **Console Tab**: Stack trace analysis and breakpoint logging.
  - **Network Tab**: Inspecting HTTP headers, payload sizes, status codes, and latency waterfalls.
  - **Application Tab**: Verifying LocalStorage entries and cookie flags.
- **Activity**: Inspect network requests on a high-traffic production website and analyze its payload timings.
- **Deliverable**: `day-39/debugging-notes.md`

---

### 📅 Day 40: 🏆 MILESTONE PROJECT #4 — Live Weather & Currency Dashboard
- **Objective**: Develop a modern dashboard application consuming a live external REST API (such as Open-Meteo or CoinGecko).
- **Feature Requirements**:
  1. Search input for global cities or crypto symbols.
  2. Live metric cards displaying current values, timestamps, and condition icons.
  3. Resilient error handling when an invalid query is submitted.
  4. "Recent Searches" history cached inside LocalStorage.
- **Verification**: Deploy live to **Vercel** or **Netlify**!
