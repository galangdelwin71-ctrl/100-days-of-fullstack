# 🎯 Days 41–50: React.js Fundamentals & State Management

Dito ninyo aaralin ang #1 Frontend Library sa buong mundo: **React.js**. Halos lahat ng tech companies ay naghahanap ng React developers.

---

### 📅 Day 41: Introduction to React & JSX
- **Konsepto**: Bakit sikat ang React?
  - Component-based architecture (parang Lego blocks).
  - JSX: Pagsasama ng HTML at JavaScript sa loob ng iisang component.
  - Virtual DOM vs Real DOM.
- **Activity**: Gumawa ng unang React component gamit ang Vite (`Header.jsx`, `Footer.jsx`).
- **Output**: `day-41-react-intro/`

---

### 📅 Day 42: React Props & Component Reusability
- **Konsepto**: Paano magpasa ng data mula sa magulang papuntang anak na component?
  - Props: `function UserCard({ name, role, avatar }) { ... }`
  - Reusing identical layouts with different data.
- **Activity**: Gumawa ng reusable `ProductCard` component at i-render ito nang 4 na beses na may magkakaibang props.
- **Output**: `day-42-props/`

---

### 📅 Day 43: React `useState`: Reactive UI
- **Konsepto**: State ang alaala ng isang component. Kapag nagbago ang state, kusa itong magre-render sa screen!
  - `const [count, setCount] = useState(0);`
  - Immutable state rules (huwag i-mutate nang direkta, laging gamitin ang setter function).
- **Activity**: Gumawa ng Like Button na may counter at toggleable heart color.
- **Output**: `day-43-usestate/`

---

### 📅 Day 44: Handling Forms & User Input in React
- **Konsepto**: Controlled Components:
  - Pag-bind ng input value sa state: `<input value={name} onChange={(e) => setName(e.target.value)} />`
  - Handling multi-input forms gamit ang single state object.
- **Activity**: Gumawa ng Sign-up Form sa React na nagva-validate bago mag-submit.
- **Output**: `day-44-react-forms/`

---

### 📅 Day 45: Conditional Rendering & Lists with Keys
- **Konsepto**: 
  - Conditional: `{isLoggedIn ? <Dashboard /> : <LoginForm />}` o `{hasError && <ErrorBanner />}`.
  - Lists: `.map((item) => <ItemCard key={item.id} {...item} />)`.
  - Bakit kailangan ng unique `key` prop?
- **Activity**: Mag-render ng listahan ng mga estudyante na may filter buttons ("All", "Passed", "Failed").
- **Output**: `day-45-lists-and-keys/`

---

### 📅 Day 46: `useEffect`: Fetching Data on Component Mount
- **Konsepto**: Paano tumawag ng API kapag bumukas ang page?
  - `useEffect(() => { fetchData(); }, []);`
  - The dependency array `[]` (kailan tumatakbo ang effect).
- **Activity**: Kumuha ng listahan ng users mula sa JSONPlaceholder at i-render sa React cards pagkabukas ng page.
- **Output**: `day-46-useeffect/`

---

### 📅 Day 47: `useEffect` Cleanups & Avoiding Memory Leaks
- **Konsepto**: Ano ang nangyayari kapag nag-unmount ang component?
  - Cleaning up event listeners, timers, at AbortController sa API calls.
- **Activity**: Gumawa ng window resize listener sa loob ng React component na may proper cleanup return function.
- **Output**: `day-47-cleanup/`

---

### 📅 Day 48: Lifting State Up
- **Konsepto**: Paano mag-share ng data ang dalawang sibling components?
  - Ilagay ang state sa pinakamalapit nilang common parent, tapos ipasa pababa bilang props at callback functions.
- **Activity**: Isang Search Bar component sa itaas na nagfi-filter sa Product List component sa ibaba.
- **Output**: `day-48-lifting-state/`

---

### 📅 Day 49: Styling React with Tailwind CSS
- **Konsepto**: Pagsamahin ang bilis ng Tailwind CSS sa loob ng React components.
  - Setting up Tailwind with Vite.
  - Creating modular UI components: `<Button variant="primary">Submit</Button>`.
- **Activity**: I-style ang isang kompleto at modernong Dashboard Navbar at Sidebar gamit ang Tailwind sa React.
- **Output**: `day-49-react-tailwind/`

---

### 📅 Day 50: 🏆 MINI-PROJECT #5 — Movie Explorer & Favorites App (React)
- **Goal**: Isang dynamic Single Page App (SPA) na gumagamit ng OMDb API o TMDB API.
- **Features**:
  1. Search input para maghanap ng pelikula.
  2. Movie cards na nagpapakita ng poster, title, at release year.
  3. "Add to Favorites" button na nag-se-save ng paboritong movies sa LocalStorage.
  4. Tab para i-view ang listahan ng Favorites.
  5. Responsive layout at loading skeleton animation.
- **Action**: I-deploy sa **Vercel** (`npm run build`) at i-share ang live link!
