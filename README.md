# 🍕 Pesto's Pizza World

A clean, responsive pizza menu web application built with **React 18**. This project demonstrates core React fundamentals alongside modern CSS techniques, making it an ideal showcase of front-end development skills.

---

## 🚀 Live Demo

> Run locally with `npm start` — see [Getting Started](#getting-started) below.

---

## 📸 Preview

The app renders a full pizza menu with:
- A styled header with decorative CSS pseudo-elements
- A menu grid showing each pizza's photo, ingredients, and price
- A time-aware footer that shows an order button only during business hours (12:00–22:00)
- Sold-out pizzas displayed in grayscale with a "SOLD OUT" badge

---

## 🛠️ Technologies & Tools

| Technology | Purpose |
|---|---|
| **React 18** | UI library — component rendering, JSX, StrictMode |
| **ReactDOM** | Mounting the React app to the DOM via `createRoot` |
| **Create React App** | Zero-config project scaffolding, build pipeline (Webpack, Babel, ESLint) |
| **JavaScript (ES6+)** | Arrow functions, destructuring, template literals, array methods |
| **JSX** | Declarative UI syntax embedded in JavaScript |
| **CSS3** | Styling — custom properties, Flexbox, CSS Grid, transitions, pseudo-elements |
| **Google Fonts** | Typography — Roboto Mono font family |
| **@testing-library/react** | Component testing utilities |
| **@testing-library/jest-dom** | Custom DOM matchers for Jest |
| **web-vitals** | Core Web Vitals performance measurement |
| **Node.js / npm** | Dependency management and script running |

---

## ⚛️ React Skills Demonstrated

### Component Architecture
The app is split into focused, single-responsibility functional components:

```
App
├── Header       — Displays the restaurant name
├── Menu         — Renders the pizza list
│   └── Pizza    — Individual pizza card (×6)
└── Footer
    └── Order    — CTA shown only during open hours
```

### Key React Concepts Used

- **Functional components** — Every UI piece is a pure function returning JSX
- **Props** — Data flows down from `Menu → Pizza` and `Footer → Order`
- **JSX** — HTML-like syntax compiled to `React.createElement` calls
- **Conditional rendering** — The footer shows different content depending on the current time; the menu shows a fallback message when the pizza list is empty
- **List rendering** — `pizzaData.map()` generates `<Pizza>` components dynamically with stable `key` props
- **Dynamic class names** — Sold-out pizzas receive a `sold-out` CSS class computed from prop values
- **React StrictMode** — Enabled at the root to surface potential issues during development
- **`ReactDOM.createRoot`** — Uses the React 18 concurrent-ready root API

---

## 🎨 CSS Skills Demonstrated

- **CSS Reset** — Universal `box-sizing: border-box` and margin/padding reset
- **Flexbox** — Used for the overall page layout (`container`), individual pizza cards, and the order section
- **CSS Grid** — Two-column `grid-template-columns: 1fr 1fr` layout for the pizza list
- **Pseudo-elements (`::before` / `::after`)** — Decorative horizontal lines flanking the header title
- **CSS transitions** — Smooth hover effect on the order button (`transition: all 0.2s`)
- **`filter: grayscale()`** — Visual indicator for sold-out items
- **Responsive typography** — Root `font-size: 62.5%` for intuitive `rem` sizing
- **Google Fonts integration** — `@import` of Roboto Mono via CSS

---

## 📁 Project Structure

```
pizza-menu-react/
├── public/
│   ├── index.html          # HTML entry point
│   ├── pizzas/             # Pizza images (JPEG)
│   └── manifest.json
├── src/
│   ├── index.js            # App entry — all React components
│   └── index.css           # All styles
├── package.json
└── README.md
```

---

## 🏁 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v16 or higher
- npm (bundled with Node.js)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/rafael-a-g-n/pizza-menu-react.git
cd pizza-menu-react

# 2. Install dependencies
npm install

# 3. Start the development server
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser. The page reloads automatically on file changes.

---

## 📜 Available Scripts

| Script | Description |
|---|---|
| `npm start` | Runs the app in development mode at `localhost:3000` |
| `npm test` | Launches the Jest test runner in interactive watch mode |
| `npm run build` | Creates an optimized production build in the `build/` folder |
| `npm run eject` | Exposes the underlying Webpack/Babel/ESLint config (one-way operation) |

---

## 🧪 Testing

Testing infrastructure is provided by **Create React App** using:

- **Jest** — Test runner
- **@testing-library/react** — React component rendering and querying utilities
- **@testing-library/jest-dom** — Extended DOM assertions (e.g., `toBeInTheDocument`)
- **@testing-library/user-event** — Simulates real user interactions

Run the tests with:

```bash
npm test
```

---

## 📦 Dependencies

```json
{
  "react": "^18.2.0",
  "react-dom": "^18.2.0",
  "react-scripts": "5.0.1",
  "@testing-library/jest-dom": "^5.17.0",
  "@testing-library/react": "^13.4.0",
  "@testing-library/user-event": "^13.5.0",
  "web-vitals": "^2.1.4"
}
```

---

## 👤 Author

**Rafael A. G. N.**
- GitHub: [@rafael-a-g-n](https://github.com/rafael-a-g-n)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
