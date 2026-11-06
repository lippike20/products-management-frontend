# Vue 3 + Tailwind CSS Starter Template

A clean, minimal, and modern starter template for building web applications with **Vue 3** (`<script setup>`), **Vite**, and **Tailwind CSS v4**.

This repository is configured as a **public template** so you can quickly spin up new projects without repeating boilerplate setup.

---

## Features

- **Vue 3.5+** — Composition API with Single-File Components (`<script setup>`)
- **Tailwind CSS v4** — Zero-config CSS-first setup via `@tailwindcss/vite`
- **Vite 6** — Instant dev server start, fast Hot Module Replacement (HMR), and optimized builds
- **Light & Dark Mode** — Automatic system theme adaptation (`color-scheme: light dark`) and dark utility classes

---

## Creating Your Own Repository from This Template

You can create a new repository with a clean commit history using any of the three methods below:

### Option 1: Using the GitHub Web UI (Recommended)

1. Click the **"Use this template"** button at the top right of the [GitHub repository page](https://github.com/MystioDev/vue-tailwindcss), then select **"Create a new repository"**.
2. Choose an **Owner**, enter your **Repository name** (e.g., `my-vue-app`), and select **Public** or **Private** visibility.
3. Click **"Create repository"**.
4. Clone your newly created repository locally:
   ```bash
   git clone https://github.com/<your-username>/<my-vue-app>.git
   cd <my-vue-app>
   ```

### Option 2: Using the GitHub CLI (`gh`)

If you have the [GitHub CLI](https://cli.github.com/) installed, you can create and clone your own repository in a single command:

```bash
gh repo create my-vue-app --template MystioDev/vue-tailwindcss --public --clone
cd my-vue-app
```

*(Replace `--public` with `--private` if you want a private repository.)*

### Option 3: Using `degit` (Local Scaffold Only)

If you want to download the template files locally without creating a GitHub repository right away:

```bash
npx degit MystioDev/vue-tailwindcss my-vue-app
cd my-vue-app
git init
```

---

## Getting Started

### Prerequisites

- **Node.js** `>= 18.0.0` (Node 20+ or 22+ recommended)
- **npm**, **pnpm**, or **yarn**

### 1. Install Dependencies

```bash
npm install
```

### 2. Start the Development Server

```bash
npm run dev
```

Open your browser at `http://localhost:5173`. Editing files in `src/` will automatically reload the page.

### 3. Build for Production

```bash
npm run build
```

The compiled, minified production assets will be generated in the `dist/` directory.

### 4. Preview Production Build Locally

```bash
npm run preview
```

---

## Project Structure

```text
vue-tailwindcss/
├── index.html                  # App entry HTML
├── package.json                # Scripts and dependencies
├── vite.config.js              # Vite + Vue + Tailwind CSS plugin config
├── public/
│   └── favicon.svg             # Static assets served at root path
└── src/
    ├── main.js                 # Vue application initialization
    ├── style.css               # Tailwind CSS import & global base styles
    ├── App.vue                 # Root Vue component
    └── components/
        └── HelloWorld.vue      # Starter example component
```

---

## Starter Snippet & Customization

### Using Vue + Tailwind in a Component

Create components inside `src/components/` using Vue's `<script setup>` syntax and Tailwind utility classes directly in your `<template>`:

```vue
<!-- src/components/CounterCard.vue -->
<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <div class="rounded-xl border border-slate-200 bg-white p-6 shadow-xs dark:border-slate-800 dark:bg-slate-900">
    <h3 class="text-lg font-semibold text-slate-900 dark:text-white">
      Interactive Counter
    </h3>
    <p class="mt-1 text-sm text-slate-600 dark:text-slate-400">
      Clicked {{ count }} {{ count === 1 ? 'time' : 'times' }}.
    </p>
    <button
      type="button"
      class="mt-4 rounded-lg bg-emerald-600 px-4 py-2 text-sm font-medium text-white transition hover:bg-emerald-500"
      @click="count++"
    >
      Increment
    </button>
  </div>
</template>
```

### Customizing Tailwind CSS Theme

Tailwind CSS v4 uses CSS-first configuration in `src/style.css`. You can define custom theme tokens using the `@theme` directive:

```css
/* src/style.css */
@import "tailwindcss";

@theme {
  --font-sans: "Inter", system-ui, sans-serif;
  --color-brand: oklch(0.65 0.18 160);
}
```

---

## License

MIT — free to use for personal and commercial projects.
