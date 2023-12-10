<template>
    <!-- navbar start -->
    <header class = "bg-navy fixed top-0 left-0 w-full flex items-center z-10">
    <div class = "container">
      <div class="flex items-center justify between relative">
        <div class="px-4 flex py-2">
          <div></div>
          <img src="../assets/image/Vector.png" alt="error">
          <a href="#" class="px-1 text-xs text-white">search.. |</a>
          <img src="../assets/image/globe.png" alt="error">
          <p class="px-1 text-xs text-white">Bahasa</p>
          <img src="../assets/image/id.png" alt="error" class="w-4 h-3 pt-1 ps-1">
          <img src="../assets/image/bawah.png" alt="error" class="w-4 h-3 pt-1 ps-1">
        </div>
      </div>
      <nav class="py-5 bg-white shadow-lg fixed left-0 w-full flex items-center z-10">
        <ul>
          <li class="text-black/50 font-bold text-base text-center px-2 flex">
            <a href="#" class="pl-16 pr-6 pt-1 hover:text-amber-600">Beranda</a>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 pt-1 hover:text-amber-600 group-hover:text">Profil</a>
                <div class=" text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'berita' }">Berita</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'sejarah' }">Sejarah Singkat</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'visimisi' }">Visi Misi Sasaran</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'manajemen' }">Manajemen</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'strukturorganisasi' }">Struktur Organisasi</NuxtLink></ul>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Akademik</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'departemen' }">Departemen</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programmagister' }">Program Magister</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programdoktor' }">Program Doktor</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programprofesi' }">Program Profesi</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'akreditasi' }">Akreditasi</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'kalenderakademik' }">Kalender Akademik</NuxtLink></ul>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Sumber Daya</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'gurubesar' }">Guru Besar</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'tenagakependidikan' }">Tenaga Kependidikan</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'saranadanprasarana' }">Sarana dan Prasarana</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'perpustakaan' }">Perpustakaan</NuxtLink></ul>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">K3</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <ul class="py-2"><NuxtLink :to="{ name: 'profilk3' }">Profil K3</NuxtLink></ul>
                    <ul class="py-2"><NuxtLink :to="{ name: 'strukturorganisasik3' }">Struktur Organisasi K3</NuxtLink></ul>
                    <ul class="py-2"><NuxtLink :to="{ name: 'tentangk3' }">Tentang K3 FT-UH</NuxtLink></ul>
                    <ul class="py-2"><NuxtLink :to="{ name: 'filependukung' }">File Pendukung</NuxtLink></ul>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Kemahasiswaan</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'asrama' }">UPT Asrama (RAMTEK)</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'aturankemahasiswaan' }">Aturan Kemahasiswaan</NuxtLink></ul>
                    <ul class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'pengumuman' }">Pengumuman</NuxtLink></ul>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Riset dan Informasi</a>
                <div class="absolute hidden bg-white text-white group-hover:block mt-5 w-max p-2 rounded shadow-lg fixed" style="background-color: navy">
                    <NuxtLink :to="{ name: 'berita' }">Berita</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Sejarah Singkat</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Visi, Misi dan Sasaran</NuxtLink><br>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Kemitraan</a>
                <div class="absolute hidden bg-white text-white group-hover:block mt-5 w-max p-2 rounded shadow-lg fixed" style="background-color: navy">
                    <NuxtLink :to="{ name: 'berita' }">Berita</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Sejarah Singkat</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Visi, Misi dan Sasaran</NuxtLink><br>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">GPM-PR</a>
                <div class="absolute hidden bg-white text-white group-hover:block mt-5 w-max p-2 rounded shadow-lg fixed" style="background-color: navy">
                    <NuxtLink :to="{ name: 'berita' }">Berita</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Sejarah Singkat</NuxtLink><br>
                    <NuxtLink :to="{ name: 'berita' }">Visi, Misi dan Sasaran</NuxtLink><br>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">COT</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <li class="py-2"><NuxtLink :to="{ name: 'cotweb' }">Cot Website</NuxtLink></li>
                    <li class="py-2"><NuxtLink :to="{ name: 'jurnalcot' }">Jurnal COT</NuxtLink></li>
                    <li class="py-2"><NuxtLink :to="{ name: 'cotnewsletter' }">COT Newsletter</NuxtLink></li>
                    <li class="py-2"><NuxtLink :to="{ name: 'uigcollaboration' }">U-I-G COLLABORATION</NuxtLink></li>
                </div>
            </div>
          </li>
        </ul>
      </nav>
    </div>
  </header>
  <!-- navbar end -->
</template>