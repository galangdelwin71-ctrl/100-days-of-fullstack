# 🎯 Days 41–50: React.js Fundamentals & State Management

In this module, you will learn the #1 frontend library in global demand: **React.js**. You will master component hierarchies, reactive state, and hook lifecycles.

---

### 📅 Day 41: Introduction to React & JSX Syntax
- **Concepts**: Why did React revolutionize web development?
  - Component-driven architecture (reusable Lego-block UI).
  - JSX: Expressing UI markup and JavaScript expressions within a unified component.
  - Virtual DOM reconciliation vs direct DOM mutation.
- **Activity**: Bootstrap a React app with Vite (`npm create vite@latest frontend -- --template react`) and write your first components.
- **Deliverable**: `day-41-react-intro/`

---

### 📅 Day 42: React Props & Component Composition
- **Concepts**: Passing data downward across the component tree:
  - Unidirectional data flow.
  - Props destructuring: `function ProductCard({ title, price, inStock }) { ... }`.
  - Reusing identical UI components with dynamic data inputs.
- **Activity**: Build a modular `MetricCard` component and render it across a dashboard with 4 distinct prop variations.
- **Deliverable**: `day-42-props/`

---

### 📅 Day 43: React `useState`: Reactive UI & Immutability
- **Concepts**: State represents the living memory of a component:
  - The `useState` hook: `const [count, setCount] = useState(0);`.
  - State immutability rules: Never mutate state directly (`state.push()` is forbidden); always pass fresh references.
- **Activity**: Build an interactive Counter and Color Palette switcher powered by reactive state.
- **Deliverable**: `day-43-usestate/`

---

### 📅 Day 44: Controlled Forms & Two-Way Binding
- **Concepts**: Managing user input within React:
  - Controlled inputs: Binding input value to state and intercepting updates via `onChange`.
  - Handling multi-field forms cleanly using a single unified state object.
- **Activity**: Build a complete Signup form with validation messages rendered conditionally in real-time.
- **Deliverable**: `day-44-react-forms/`

---

### 📅 Day 45: Conditional Rendering & List Keys
- **Concepts**: Dynamic rendering patterns:
  - Inline conditionals: `{isAuthorized ? <Dashboard /> : <AccessDenied />}` and `{error && <ErrorAlert />}`.
  - Array iteration: `.map((item) => <ItemRow key={item.id} {...item} />)`.
  - Why stable, unique `key` props prevent rendering glitches.
- **Activity**: Render a filtered list of products with category pill filters ("All", "Tech", "Apparel").
- **Deliverable**: `day-45-lists-and-keys/`

---

### 📅 Day 46: `useEffect`: Data Fetching on Component Mount
- **Concepts**: Managing side effects in functional components:
  - When does `useEffect` run?
  - The dependency array `[]` (mount lifecycle).
  - Fetching remote REST API data inside `useEffect` and storing it in state.
- **Activity**: Fetch a list of user records from an API and render them into responsive cards on page load.
- **Deliverable**: `day-46-useeffect/`

---

### 📅 Day 47: Effect Cleanups & Memory Leak Prevention
- **Concepts**: Cleaning up after unmounted components:
  - Returning a cleanup callback function inside `useEffect`.
  - Disconnecting event listeners, clearing timers, and aborting fetch calls via `AbortController`.
- **Activity**: Construct a live window resize listener component that properly cleans up its listener on unmount.
- **Deliverable**: `day-47-cleanup/`

---

### 📅 Day 48: Lifting State Up
- **Concepts**: Sharing state between sibling components:
  - Moving shared state up to the closest common parent component.
  - Passing down state as props, and passing update handler functions as callbacks.
- **Activity**: Build a parent layout where a child `SearchBar` component filters a sibling `UserList` component.
- **Deliverable**: `day-48-lifting-state/`

---

### 📅 Day 49: Styling React with Tailwind CSS
- **Concepts**: Merging React component architecture with Tailwind utility styling:
  - Configuring Tailwind inside a Vite + React application.
  - Creating modular design components: `<Button variant="danger">Delete</Button>`.
- **Activity**: Style a modern Dashboard Sidebar and App Header using Tailwind CSS inside your React app.
- **Deliverable**: `day-49-react-tailwind/`

---

### 📅 Day 50: 🏆 MILESTONE PROJECT #5 — React Movie Search & Favorites App
- **Objective**: Build a responsive Single Page Application (SPA) using React, Tailwind CSS, and a public movie API (such as OMDb or TMDB).
- **Feature Requirements**:
  1. Real-time debounced movie title search.
  2. Movie cards displaying poster imagery, release year, and genre tags.
  3. "Favorite" bookmarking action persisted to LocalStorage.
  4. Filter tab allowing users to toggle between "All Results" and "My Favorites".
  5. Animated loading skeletons and empty search fallback states.
- **Verification**: Build the production bundle (`npm run build`) and deploy live to **Vercel**!
