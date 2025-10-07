<template>
  <section class="mx-auto max-w-6xl px-6 lg:px-8">
    <div class="rounded-3xl border border-white/5 bg-slate-900/40 p-10 shadow-lg shadow-primary-500/10 backdrop-blur">
      <div class="grid gap-10 md:grid-cols-2 lg:grid-cols-4">
        <article v-for="stat in stats" :key="stat.label" class="space-y-3">
          <p class="text-xs uppercase tracking-[0.3em] text-primary-200">{{ stat.category }}</p>
          <p class="text-3xl font-semibold text-white">{{ stat.value }}</p>
          <p class="text-sm text-slate-300">{{ stat.label }}</p>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  {
    category: 'Pelayanan',
    value: '98% puas',
    label: 'Respon cepat & ramah berdasarkan survei Indeks Kepuasan Masyarakat 2024',
  },
  {
    category: 'Digitalisasi',
    value: '100%',
    label: 'Seluruh alur administrasi sudah terintegrasi dengan sistem SIMKAH',
  },
  {
    category: 'Pendampingan',
    value: '24/7',
    label: 'Layanan konsultasi daring & hotline petugas KUA siap membantu kapan pun',
  },
  {
    category: 'Jangkauan',
    value: '5 kelurahan',
    label: 'Penjaringan, Pluit, Pejagalan, Ancol, dan Kamal Muara dalam satu kecamatan',
  },
];
</script>
