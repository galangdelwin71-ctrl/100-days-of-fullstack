# 🎯 Days 31–40: Modern JavaScript, Async/Await & APIs

Sa phase na ito, matututunan mo kung paano kumuha ng totoong data mula sa internet gamit ang REST APIs, at ang mga modern tools na ginagamit sa industriya tulad ng Vite at Git.

---

### 📅 Day 31: Asynchronous JavaScript & The Event Loop
- **Konsepto**: Bakit single-threaded ang JavaScript pero kaya nitong mag-download habang gumagalaw ang UI?
  - Call Stack, Web APIs, Callback Queue, at Event Loop.
  - `setTimeout` at `setInterval`.
- **Activity**: Gumawa ng digital clock na nag-u-update bawat segundo gamit ang `setInterval`.
- **Output**: `day-31/clock.html`

---

### 📅 Day 32: JavaScript Promises & Error Handling
- **Konsepto**: Paano iwasan ang "Callback Hell"?
  - States ng Promise: `Pending`, `Fulfilled`, `Rejected`.
  - `.then()`, `.catch()`, at `.finally()`.
- **Activity**: Gumawa ng custom promise na nag-si-simulate ng coin toss (50% success, 50% error).
- **Output**: `day-32/promises.js`

---

### 📅 Day 33: Async / Await Syntax
- **Konsepto**: Ang modern at pinakamalinis na paraan para humawak ng asynchronous code.
  - `async function fetchData() { ... }`
  - `try { const data = await ... } catch (error) { ... }`
- **Activity**: I-refactor ang Day 32 promise code papuntang malinis na `async/await` syntax.
- **Output**: `day-33/async-await.js`

---

### 📅 Day 34: Fetch API: Getting Data from Public APIs
- **Konsepto**: Kumuha ng live data mula sa internet!
  - `fetch('https://api.example.com/data')`
  - Pag-parse ng response: `const data = await response.json();`
- **Activity**: Kumuha ng data mula sa libreng public API (hal. [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts) o Random Quote API) at i-render sa UI.
- **Output**: `day-34/fetch-quotes.html`

---

### 📅 Day 35: Fetch API: POST, PUT & DELETE
- **Konsepto**: Pagpapadala ng data pabalik sa server.
  - Method: `POST`, `PUT`, `DELETE`.
  - Headers: `'Content-Type': 'application/json'`.
  - Body: `JSON.stringify(payload)`.
- **Activity**: Gumawa ng form na nagpapadala ng dummy POST request sa JSONPlaceholder API.
- **Output**: `day-35/fetch-post.html`

---

### 📅 Day 36: Handling API States: Loading, Error & Empty
- **Konsepto**: Ang pinagkaiba ng baguhan sa professional:
  - Huwag iwang blanko ang screen habang naglo-load!
  - Ipakita ang Loading Spinner habang naghihintay.
  - Magpakita ng User-Friendly Error message kapag walang internet o 404.
- **Activity**: Gumawa ng API fetcher na may complete UI states (Loading indicator, Error banner, at Success card).
- **Output**: `day-36/api-states.html`

---

### 📅 Day 37: Modern Tooling: Node.js, NPM & Vite
- **Konsepto**: Bakit hindi na tayo nag-do-double click lang ng HTML file sa desktop?
  - Package manager: `npm init`, `npm install`.
  - Vite: Ang pinakamabilis na modern frontend build tool.
- **Activity**: Mag-install ng Node.js sa inyong computer. Gumawa ng bagong Vite project gamit ang terminal: `npm create vite@latest my-app`.
- **Output**: Screenshot o repo ng gumaganang Vite dev server (`http://localhost:5173`).

---

### 📅 Day 38: Git Team Workflow: Branches, Pull Requests & Conflicts
- **Konsepto**: Paano mag-collaborate sa code ang magkaibigan nang hindi nagkakagulo?
  - `git checkout -b feature/navbar`
  - `git push origin feature/navbar`
  - Paggawa ng Pull Request (PR) sa GitHub at pag-merge.
- **Activity**: Gumawa kayo ng kaibigan mo ng shared repo. Si Friend A gagawa ng branch para sa Header, si Friend B gagawa ng branch para sa Footer. I-merge ninyo pareho!
- **Output**: Closed Pull Request sa GitHub repo ninyo.

---

### 📅 Day 39: Chrome DevTools Deep Dive
- **Konsepto**: Ang paboritong tool ng bawat web developer:
  - **Console tab**: Error tracing.
  - **Network tab**: Pagtingin sa API request payload, status codes (200, 400, 401, 500), at response time.
  - **Application tab**: Pag-inspect ng LocalStorage at Cookies.
- **Activity**: Buksan ang Network tab at i-inspect ang isang live website habang naglo-load.
- **Output**: `day-39/notes.md` na naglalaman ng inyong natutunang diagnostics.

---

### 📅 Day 40: 🏆 MINI-PROJECT #4 — Real-Time Weather or Crypto Tracker
- **Goal**: Isang modernong web app na kumukuha ng live data mula sa isang totoong external API (halimbawa: Open-Meteo API o CoinGecko API).
- **Features**:
  1. Search bar para sa Lungsod o Currency.
  2. Live weather card (Temperature, Humidity, Wind speed, Weather icon).
  3. Error handling kung mali ang spelling ng lungsod.
  4. Kamakailang hinanap (Recent Searches) na naka-save sa LocalStorage.
- **Action**: I-deploy sa **Vercel** o **GitHub Pages**!
