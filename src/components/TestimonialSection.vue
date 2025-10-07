<template>
  <section class="mx-auto max-w-6xl px-6 lg:px-8">
    <div class="rounded-3xl border border-white/10 bg-slate-900/60 p-10 lg:p-14">
      <div class="grid gap-10 lg:grid-cols-[1fr_1.1fr] lg:items-center">
        <div class="space-y-4">
          <p class="text-xs uppercase tracking-[0.3em] text-primary-200">Cerita warga</p>
          <h2 class="font-display text-3xl font-semibold text-white sm:text-4xl">Pendampingan ramah dan proses terasa mudah</h2>
          <p class="text-base text-slate-300">
            Komitmen kami adalah memberikan pelayanan terbaik dengan memadukan teknologi dan sentuhan personal dari para penghulu, penyuluh, dan staf KUA Penjaringan.
          </p>
          <div class="flex items-center gap-4 rounded-2xl border border-white/10 bg-white/5 p-5">
            <div class="flex h-12 w-12 items-center justify-center rounded-full bg-primary-500/20 text-lg font-semibold text-primary-100">
              4.9
            </div>
            <div>
              <p class="text-sm font-semibold text-white">Indeks Kepuasan Masyarakat</p>
              <p class="text-xs text-slate-400">Survei triwulan IV tahun 2024</p>
            </div>
          </div>
        </div>
        <div class="space-y-6">
          <article
            v-for="testimonial in testimonials"
            :key="testimonial.name"
            class="rounded-3xl border border-white/10 bg-slate-950/60 p-6 shadow-lg shadow-primary-500/10"
          >
            <p class="text-sm text-slate-200">“{{ testimonial.quote }}”</p>
            <div class="mt-4 flex items-center justify-between">
              <div>
                <p class="text-sm font-semibold text-white">{{ testimonial.name }}</p>
                <p class="text-xs text-slate-400">{{ testimonial.role }}</p>
              </div>
              <div class="flex gap-1 text-primary-300">
                <svg
                  v-for="star in 5"
                  :key="star"
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path d="M12 4.75 13.89 9h4.61l-3.73 2.71 1.42 4.54L12 15.67l-4.19 3 1.42-4.54L5.5 9h4.61L12 4.75Z" />
                </svg>
              </div>
            </div>
          </article>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    name: 'Raka & Nadya',
    role: 'Warga Pluit',
    quote: 'Petugasnya membantu menyiapkan berkas dan menjelaskan prosedur dengan sabar. Kami merasa sangat terbantu.',
  },
  {
    name: 'Evelyn',
    role: 'Penyuluh Agama Mitra',
    quote: 'Kolaborasi dengan KUA Penjaringan memudahkan kami memberikan edukasi keluarga sakinah bagi pasangan muda.',
  },
  {
    name: 'Yusuf & Mira',
    role: 'Warga Pejagalan',
    quote: 'Bimbingan calon pengantin sangat bermanfaat dan membuat kami lebih siap membangun keluarga.',
  },
];
</script>
