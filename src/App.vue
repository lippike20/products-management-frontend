<script setup>
import HelloWorld from './components/HelloWorld.vue'

const features = [
  {
    title: 'Vue 3 Composition API',
    description: 'Built with single-file components (<script setup>) and reactive primitives out of the box.',
    badge: 'Vue 3.5+',
  },
  {
    title: 'Tailwind CSS v4',
    description: 'Zero-configuration CSS-first styling powered by the official @tailwindcss/vite plugin.',
    badge: 'Tailwind v4',
  },
  {
    title: 'Instant Vite Tooling',
    description: 'Lightning-fast dev server startup, instant Hot Module Replacement, and optimized production builds.',
    badge: 'Vite 6',
  },
]
</script>

<template>
  <div class="flex min-h-dvh flex-col justify-between px-6 py-12 sm:px-8 lg:px-12">
    <header class="mx-auto flex w-full max-w-5xl items-center justify-between">
      <div class="flex items-center gap-2.5 font-semibold tracking-tight text-slate-900 dark:text-white">
        <span class="inline-flex size-8 items-center justify-center rounded-lg bg-slate-900 text-sm font-bold text-emerald-400 dark:bg-slate-800">
          V
        </span>
        <span>vue-tailwindcss</span>
      </div>
      <nav aria-label="Documentation links" class="flex items-center gap-4 text-sm font-medium text-slate-600 dark:text-slate-400">
        <a
          href="https://vuejs.org"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex min-h-6 min-w-6 items-center hover:text-emerald-600 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-emerald-600 dark:hover:text-emerald-400"
        >
          Vue Docs
        </a>
        <a
          href="https://tailwindcss.com"
          target="_blank"
          rel="noopener noreferrer"
          class="inline-flex min-h-6 min-w-6 items-center hover:text-sky-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-sky-500 dark:hover:text-sky-400"
        >
          Tailwind Docs
        </a>
      </nav>
    </header>

    <main class="mx-auto my-16 w-full max-w-5xl">
      <HelloWorld
        title="Build fast with Vue & Tailwind CSS"
        subtitle="A minimal, zero-bloat starter template ready for your next web application. Clone or generate a new repository from this template in seconds."
      />

      <div class="mt-16 grid gap-6 sm:grid-cols-3">
        <article
          v-for="feature in features"
          :key="feature.title"
          class="rounded-2xl border border-slate-200/80 bg-white p-6 shadow-xs transition hover:border-emerald-500/40 dark:border-slate-800 dark:bg-slate-900/70"
        >
          <span class="inline-block rounded-md bg-slate-100 px-2.5 py-1 font-mono text-xs font-medium text-slate-700 dark:bg-slate-800 dark:text-slate-300">
            {{ feature.badge }}
          </span>
          <h2 class="mt-4 text-lg font-semibold text-slate-900 dark:text-white">
            {{ feature.title }}
          </h2>
          <p class="mt-2 text-sm leading-relaxed text-slate-600 dark:text-slate-400">
            {{ feature.description }}
          </p>
        </article>
      </div>
    </main>

    <footer class="mx-auto w-full max-w-5xl border-t border-slate-200/80 pt-6 text-center text-xs text-slate-500 dark:border-slate-800/80 dark:text-slate-400">
      <p>Released as a public starter template. Customize freely for your projects.</p>
    </footer>
  </div>
</template>
