<template>
  <section id="services" class="mx-auto max-w-6xl px-6 lg:px-8">
    <div class="space-y-4 text-center">
      <p class="text-xs uppercase tracking-[0.3em] text-primary-200">Layanan unggulan</p>
      <h2 class="font-display text-3xl font-semibold text-white sm:text-4xl">Pelayanan terpadu bagi masyarakat Penjaringan</h2>
      <p class="mx-auto max-w-3xl text-base text-slate-300">
        Semua kebutuhan pencatatan pernikahan, pelayanan keagamaan, dan pemberdayaan keluarga terpenuhi dengan sistem yang mudah diakses.
      </p>
    </div>
    <div class="mt-14 grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      <article
        v-for="service in services"
        :key="service.title"
        class="group relative overflow-hidden rounded-3xl border border-white/10 bg-slate-900/60 p-8 transition duration-300 hover:-translate-y-2 hover:border-primary-400/40 hover:bg-slate-900"
      >
        <div class="flex h-12 w-12 items-center justify-center rounded-2xl bg-primary-500/10 text-primary-300">
          <component :is="service.icon" class="h-6 w-6" />
        </div>
        <h3 class="mt-6 font-display text-xl font-semibold text-white">{{ service.title }}</h3>
        <p class="mt-3 text-sm text-slate-300">{{ service.description }}</p>
        <ul class="mt-6 space-y-2 text-xs text-slate-400">
          <li v-for="item in service.items" :key="item" class="flex items-center gap-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5 text-primary-300" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.6" d="m5 12 4 4L19 6" />
            </svg>
            {{ item }}
          </li>
        </ul>
      </article>
    </div>
  </section>
</template>

<script setup>
import { defineComponent, h } from 'vue';

const iconProps = {
  viewBox: '0 0 24 24',
  fill: 'none',
  stroke: 'currentColor',
  class: 'h-6 w-6',
};

const IconBookShield = defineComponent({
  name: 'IconBookShield',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M12 5.5 6 9v10l6 3.5 6-3.5V9l-6-3.5Z',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M6 9l6 3.5 6-3.5',
        }),
      ]);
  },
});

const IconHandshake = defineComponent({
  name: 'IconHandshake',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M7 9c1.333-1.333 3.667-1.333 5 0m0 0c1.333-1.333 3.667-1.333 5 0m-5 0v6',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M12 15c-1.333 1.333-3.667 1.333-5 0M12 15c1.333 1.333 3.667 1.333 5 0',
        }),
      ]);
  },
});

const IconMosque = defineComponent({
  name: 'IconMosque',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'm3 7 9-5 9 5v10l-9 5-9-5V7Z',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M9 21V9l6-3',
        }),
      ]);
  },
});

const IconArrowLoop = defineComponent({
  name: 'IconArrowLoop',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'm5 5 7 7-7 7',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M12 5h7v14h-7',
        }),
      ]);
  },
});

const IconBuilding = defineComponent({
  name: 'IconBuilding',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M12 3v3m0 0-7 4v11h14V10l-7-4Z',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M5 10h14',
        }),
      ]);
  },
});

const IconChat = defineComponent({
  name: 'IconChat',
  setup() {
    return () =>
      h('svg', iconProps, [
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M12 20a8 8 0 1 0-8-8 8 8 0 0 0 8 8Z',
        }),
        h('path', {
          'stroke-linecap': 'round',
          'stroke-linejoin': 'round',
          'stroke-width': 1.5,
          d: 'M8.5 14.5a3.5 3.5 0 0 1 7 0v1a1.5 1.5 0 0 1-3 0',
        }),
      ]);
  },
});

const services = [
  {
    title: 'Pencatatan Pernikahan',
    description: 'Pendampingan lengkap dari pendaftaran SIMKAH, pemeriksaan berkas, hingga pelaksanaan akad nikah.',
    items: ['Pendaftaran daring & luring', 'Jadwal akad fleksibel', 'Bimbingan calon pengantin'],
    icon: IconBookShield,
  },
  {
    title: 'Bimbingan Keluarga',
    description: 'Program edukasi dan pendampingan keluarga sakinah untuk calon pengantin dan pasangan muda.',
    items: ['Kelas tatap muka & online', 'Materi narasumber profesional', 'Pendamping pasca nikah'],
    icon: IconHandshake,
  },
  {
    title: 'Pelayanan Keagamaan',
    description: 'Administrasi keagamaan mulai dari rekomendasi haji, konsultasi zakat, hingga wakaf.',
    items: ['Rekomendasi haji & umrah', 'Legalisasi surat keagamaan', 'Pendampingan zakat & wakaf'],
    icon: IconMosque,
  },
  {
    title: 'Pelayanan Kepenghuluan',
    description: 'Petugas penghulu profesional siap membantu pelaksanaan akad nikah di lokasi pilihan Anda.',
    items: ['Jadwal fleksibel', 'Dokumentasi berita acara', 'Koordinasi dengan pihak terkait'],
    icon: IconArrowLoop,
  },
  {
    title: 'Administrasi Masjid',
    description: 'Pendataan dan pembinaan masjid/musala di wilayah kecamatan Penjaringan.',
    items: ['Sertifikasi tanah wakaf', 'Pendampingan legalitas', 'Pelatihan manajemen masjid'],
    icon: IconBuilding,
  },
  {
    title: 'Layanan Konseling',
    description: 'Konsultasi keagamaan dan keluarga dengan penyuluh agama Islam berpengalaman.',
    items: ['Sesi privat & kelompok', 'Pendekatan psikologi Islam', 'Rujukan lembaga mitra'],
    icon: IconChat,
  },
];
</script>
