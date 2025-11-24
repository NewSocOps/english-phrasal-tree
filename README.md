# English Phrasal Tree

A React + Vite web application for exploring English phrasal verbs.

## 🚀 Live Demo

Visit the live application at: [https://newsocops.github.io/english-phrasal-tree/](https://newsocops.github.io/english-phrasal-tree/)

## 📦 Development

### Prerequisites

- Node.js 20 or higher
- npm

### Installation

```bash
npm install
```

### Running Locally

```bash
npm run dev
```

### Building for Production

```bash
npm run build
```

### Linting

```bash
npm run lint
```

## 🚢 Deployment

This project is automatically deployed to GitHub Pages when changes are pushed to the `main` branch.

### ⚠️ GitHub Pages Setup Required

**Before the first deployment, you must enable GitHub Pages in the repository settings:**

1. Go to repository **Settings** → **Pages**
2. Under **Build and deployment** → **Source**, select **GitHub Actions**
3. Save the changes

📋 **For detailed setup instructions, see [GITHUB_PAGES_SETUP.md](./GITHUB_PAGES_SETUP.md)**

### Deployment Workflow

Once GitHub Pages is enabled, the deployment workflow automatically:

1. Builds the application using Vite
2. Uploads the built files to GitHub Pages
3. Deploys to `https://newsocops.github.io/english-phrasal-tree/`

The workflow is triggered on:
- Every push to the `main` branch
- Manual trigger via Actions tab (workflow_dispatch)

## 🛠️ Tech Stack

- **React 19** - UI framework
- **Vite 7** - Build tool and dev server
- **Tailwind CSS 4** - Styling
- **Framer Motion** - Animations
- **Lucide React** - Icons

## 📝 React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
