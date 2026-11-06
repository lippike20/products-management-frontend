<script setup>
import { ref } from 'vue'

defineProps({
  title: {
    type: String,
    required: true,
  },
  subtitle: {
    type: String,
    default: '',
  },
})

const count = ref(0)
</script>

<template>
  <section class="mx-auto max-w-3xl text-center">
    <div class="mb-4 inline-flex items-center gap-2 rounded-full border border-emerald-500/20 bg-emerald-500/10 px-3.5 py-1 text-xs font-medium text-emerald-700 dark:text-emerald-300">
      <span class="size-2 rounded-full bg-emerald-500" aria-hidden="true"></span>
      Vue 3 + Vite + Tailwind CSS v4
    </div>

    <h1 class="text-4xl font-bold tracking-tight text-slate-900 sm:text-5xl dark:text-white">
      {{ title }}
    </h1>

    <p v-if="subtitle" class="mx-auto mt-4 max-w-xl text-base leading-relaxed text-slate-600 sm:text-lg dark:text-slate-400">
      {{ subtitle }}
    </p>

    <div class="mt-8 flex flex-wrap items-center justify-center gap-4">
      <button
        type="button"
        class="inline-flex min-h-10 min-w-10 cursor-pointer items-center justify-center gap-2 rounded-lg bg-emerald-600 px-5 py-2.5 text-sm font-semibold text-white shadow-xs transition hover:bg-emerald-500 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-emerald-600 active:scale-[0.99]"
        @click="count++"
      >
        Count is {{ count }}
      </button>

      <a
        href="https://github.com/MystioDev/vue-tailwindcss"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex min-h-10 min-w-10 items-center justify-center gap-2 rounded-lg border border-slate-300 bg-white px-5 py-2.5 text-sm font-semibold text-slate-700 shadow-xs transition hover:bg-slate-50 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-emerald-600 dark:border-slate-800 dark:bg-slate-900 dark:text-slate-200 dark:hover:bg-slate-800"
      >
        Use Template on GitHub
      </a>
    </div>

    <p class="mt-6 text-sm text-slate-500 dark:text-slate-400">
      Edit
      <code class="rounded-md bg-slate-200/70 px-1.5 py-0.5 font-mono text-xs text-slate-800 dark:bg-slate-800 dark:text-slate-200">src/App.vue</code>
      or
      <code class="rounded-md bg-slate-200/70 px-1.5 py-0.5 font-mono text-xs text-slate-800 dark:bg-slate-800 dark:text-slate-200">src/components/HelloWorld.vue</code>
      to test Hot Module Replacement (HMR).
    </p>
  </section>
</template>
