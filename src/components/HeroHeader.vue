<template>
  <header class="relative z-20">
    <div class="mx-auto flex max-w-6xl items-center justify-between px-6 py-8 lg:px-8">
      <div class="flex items-center gap-3">
        <span class="flex h-12 w-12 items-center justify-center rounded-2xl bg-primary-500/10 text-2xl font-bold text-primary-400 shadow-glow">
          KP
        </span>
        <div>
          <p class="font-display text-xl font-semibold tracking-tight text-white">KUA Penjaringan</p>
          <p class="text-sm text-slate-400">Kantor Urusan Agama Kec. Penjaringan</p>
        </div>
      </div>
      <nav class="hidden items-center gap-8 text-sm font-medium text-slate-300 lg:flex">
        <a class="transition hover:text-white" href="#services">Layanan</a>
        <a class="transition hover:text-white" href="#process">Prosedur</a>
        <a class="transition hover:text-white" href="#pricing">Biaya</a>
        <a class="transition hover:text-white" href="#contact">Kontak</a>
      </nav>
      <a
        href="https://wa.me/6281234567890"
        class="hidden rounded-full bg-white px-6 py-3 text-sm font-semibold text-slate-900 shadow-lg shadow-primary-500/20 transition hover:-translate-y-0.5 hover:shadow-xl hover:shadow-primary-500/30 lg:inline-flex"
      >
        Konsultasi Gratis
      </a>
      <button class="lg:hidden">
        <span class="sr-only">Menu</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </div>
  </header>
</template>
