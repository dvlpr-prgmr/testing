<template>
  <section id="process" class="mx-auto max-w-6xl px-6 lg:px-8">
    <div class="grid gap-12 lg:grid-cols-[1fr_1.2fr] lg:items-start">
      <div class="space-y-6">
        <p class="text-xs uppercase tracking-[0.3em] text-primary-200">Proses digital</p>
        <h2 class="font-display text-3xl font-semibold text-white sm:text-4xl">Alur pendaftaran pernikahan yang terintegrasi</h2>
        <p class="text-base text-slate-300">
          Kami memadukan sistem daring SIMKAH dengan pendampingan tatap muka agar calon pengantin dapat menyelesaikan seluruh tahapan secara efisien dan sesuai regulasi Kementerian Agama.
        </p>
        <div class="space-y-5 rounded-3xl border border-white/10 bg-slate-900/60 p-6">
          <div class="flex items-start gap-4">
            <span class="flex h-10 w-10 items-center justify-center rounded-full bg-primary-500/10 text-sm font-semibold text-primary-200">Tip</span>
            <p class="text-sm text-slate-300">
              Pastikan seluruh dokumen kependudukan sudah sinkron di Dukcapil untuk mempercepat verifikasi.
            </p>
          </div>
          <div class="flex items-start gap-4">
            <span class="flex h-10 w-10 items-center justify-center rounded-full bg-primary-500/10 text-sm font-semibold text-primary-200">Info</span>
            <p class="text-sm text-slate-300">
              Jadwal bimbingan calon pengantin dapat dipilih sesuai batch yang tersedia, maksimal H-10 sebelum akad.
            </p>
          </div>
        </div>
      </div>
      <ol class="relative space-y-8 border-l border-white/10 pl-10">
        <li
          v-for="(step, index) in steps"
          :key="step.title"
          class="group relative"
        >
          <span
            class="absolute -left-5 flex h-10 w-10 items-center justify-center rounded-full border border-primary-400/30 bg-slate-950 text-sm font-semibold text-primary-200 shadow-lg shadow-primary-500/20"
          >
            {{ index + 1 }}
          </span>
          <div class="rounded-3xl border border-white/10 bg-slate-900/60 p-6 transition duration-300 group-hover:border-primary-400/40">
            <div class="flex items-center justify-between gap-4">
              <h3 class="font-display text-xl font-semibold text-white">{{ step.title }}</h3>
              <span class="text-xs font-medium uppercase tracking-[0.3em] text-primary-200">{{ step.badge }}</span>
            </div>
            <p class="mt-3 text-sm text-slate-300">{{ step.description }}</p>
            <ul class="mt-4 space-y-2 text-xs text-slate-400">
              <li v-for="item in step.items" :key="item" class="flex items-center gap-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-3.5 w-3.5 text-primary-300" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.6" d="m5 12 4 4L19 6" />
                </svg>
                {{ item }}
              </li>
            </ul>
          </div>
        </li>
      </ol>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    title: 'Registrasi SIMKAH Online',
    badge: 'H-30',
    description: 'Calon pengantin melakukan pendaftaran mandiri di SIMKAH Kemenag dan memilih jadwal akad serta lokasi.',
    items: ['Upload dokumen KTP, KK, dan surat pengantar', 'Mengisi formulir data calon pasangan', 'Memilih jadwal bimbingan'],
  },
  {
    title: 'Validasi Berkas & Konsultasi',
    badge: 'H-20',
    description: 'Petugas KUA melakukan pengecekan dokumen, memberikan konsultasi, dan mengeluarkan rekomendasi kelurahan.',
    items: ['Verifikasi data kependudukan', 'Penjadwalan pemeriksaan kesehatan', 'Konsultasi pra-nikah individual'],
  },
  {
    title: 'Bimbingan Calon Pengantin',
    badge: 'H-10',
    description: 'Calon pengantin mengikuti kelas bimbingan keluarga sakinah secara tatap muka dan menerima modul digital.',
    items: ['Materi pembekalan keluarga sakinah', 'Simulasi pengisian buku nikah', 'Sesi tanya jawab dengan narasumber'],
  },
  {
    title: 'Pelaksanaan Akad & Dokumentasi',
    badge: 'H',
    description: 'Petugas penghulu memimpin akad nikah dan memastikan seluruh berkas tercatat serta buku nikah diterbitkan.',
    items: ['Penghulu resmi KUA Penjaringan', 'Dokumentasi berita acara & saksi', 'Pencetakan buku nikah digital & fisik'],
  },
];
</script>
