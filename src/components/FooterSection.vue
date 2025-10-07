<template>
  <footer class="border-t border-white/5 bg-slate-950/90 py-16">
    <div class="mx-auto flex max-w-6xl flex-col gap-10 px-6 text-sm text-slate-400 lg:flex-row lg:items-start lg:justify-between lg:px-8">
      <div class="max-w-md space-y-4">
        <div class="flex items-center gap-3">
          <span class="flex h-12 w-12 items-center justify-center rounded-2xl bg-primary-500/10 text-2xl font-bold text-primary-300">KP</span>
          <div>
            <p class="font-display text-xl font-semibold text-white">KUA Penjaringan</p>
            <p class="text-xs text-slate-400">Kementerian Agama Kota Administrasi Jakarta Utara</p>
          </div>
        </div>
        <p>
          Memberikan pelayanan pencatatan pernikahan, bimbingan keluarga sakinah, dan administrasi keagamaan untuk masyarakat Kecamatan Penjaringan.
        </p>
      </div>
      <div class="grid flex-1 gap-10 sm:grid-cols-2 lg:grid-cols-3">
        <div class="space-y-4">
          <p class="text-xs uppercase tracking-[0.3em] text-white/70">Kontak</p>
          <ul class="space-y-2">
            <li>Telp: (021) 6600-789</li>
            <li>Email: kuapenjaringan@kemenag.go.id</li>
            <li>WhatsApp: 0812-3456-7890</li>
          </ul>
        </div>
        <div class="space-y-4">
          <p class="text-xs uppercase tracking-[0.3em] text-white/70">Layanan</p>
          <ul class="space-y-2">
            <li>Pendaftaran pernikahan SIMKAH</li>
            <li>Bimbingan calon pengantin</li>
            <li>Konsultasi keluarga sakinah</li>
            <li>Administrasi masjid dan wakaf</li>
          </ul>
        </div>
        <div class="space-y-4">
          <p class="text-xs uppercase tracking-[0.3em] text-white/70">Alamat</p>
          <p>Jl. Muara Baru No. 3, Penjaringan, Jakarta Utara 14440</p>
          <p class="text-xs text-slate-500">© {{ new Date().getFullYear() }} KUA Penjaringan. All rights reserved.</p>
        </div>
      </div>
    </div>
  </footer>
</template>
