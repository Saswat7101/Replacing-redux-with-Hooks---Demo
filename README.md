# Replacing Redux with Hooks

[![React](https://img.shields.io/badge/React-19-green.svg)](https://react.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![React Router](https://img.shields.io/badge/React_Router-5-orange.svg)](https://reactrouter.com/)

Documents the step-by-step evolution from Context API to custom Hooks store.

## 🚀 Quick Start

### Prerequisites

- Node.js (v14+)
- npm or yarn

### Installation

1. Clone or download the repository:
   ```
   git clone <repo-url>
   cd replacing-redux-with-hooks
   ```
2. Install dependencies:
   ```
   npm install
   ```
3. Start the development server:

   ```
   npm start
   ```

   The app will open at [http://localhost:3000](http://localhost:3000)

### Build for Production

```
npm run build
```

## ✨ Features

- Products catalog with toggle favorite functionality
- Favorites page filtering favorite products
- Responsive navigation between Products and Favorites
- Dual state management implementations (Redux + Hooks/Context)

## 🛤️ Development Journey (Summary)

The project development followed this progression:

1. Implemented React Context API + useState as Redux alternative for toggling product favorites.
2. Developed custom Hooks-based store (`hooks-store`), starting with basic setup.
3. Created concrete store implementation with actions (e.g., TOGGLE_FAV).
4. Integrated and activated the custom store in the app.
5. Optimized the custom hook store for production use.

This hands-on journey demonstrates practical steps to replace Redux with lightweight Hooks solutions.

## 🏗️ Project Structure

```
src/
├── App.js                 # Main app with routing
├── components/            # Reusable UI components
│   ├── Nav/              # Navigation bar
│   ├── Products/         # Product item components
│   ├── Favorites/        # Favorite item components
│   └── UI/               # Generic UI components (Card)
├── containers/           # Page components
│   ├── Products.js       # Products page
│   └── Favorites.js      # Favorites page
├── hooks-store/          # Custom Hooks state management (replacement for Redux)
│   ├── store.js          # Core store logic
│   └── products-store.js # Products-specific store config
├── Context/              # React Context API implementation
│   └── products-context.js
└── store/                # Legacy Redux implementation (for comparison)
    ├── actions/
    └── reducers/
```

## 🔄 State Management Migration

This project showcases two approaches:

### 1. Legacy Redux (`src/store/`)

Traditional Redux with actions and reducers.

### 2. Custom Hooks Store (`src/hooks-store/`) **[Active Implementation]**

- `initStore(actions, initialState)` - Initializes global store (replaces Redux store)
- Action-based dispatch pattern (TOGGLE_FAV)
- Configured in `src/index.js` via `configureProductsStore()`

### 3. React Context + useState (`src/Context/`)

Pure Hooks/Context implementation for comparison.

## 📱 Pages & Components

- **Products Page (`/`)**: Lists all products with toggle favorite
- **Favorites Page (`/favorites`)**: Shows only favorited products
- **Navigation**: Links between pages

## 🛠️ Tech Stack

- React 19
- React Router DOM 5
- React Scripts (Create React App)
- Custom Hooks for state (hooks-store)
- React Context API
- Redux (legacy reference)
- CSS Modules for styling

## 📝 Development Scripts

| Script          | Description                 |
| --------------- | --------------------------- |
| `npm start`     | Start development server    |
| `npm run build` | Build for production        |
| `npm test`      | Run tests                   |
| `npm run eject` | Eject from Create React App |

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the MIT License.

## 🙌 Acknowledgments

Built as part of React Bootcamp to demonstrate modern state management patterns.

---

⭐ **Star this repo if you found it helpful!**
