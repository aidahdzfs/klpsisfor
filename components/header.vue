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
            <p class="pl-16 pr-6 pt-1 hover:text-amber-600"><NuxtLink to="/">Beranda</NuxtLink></p>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 pt-1 hover:text-amber-600 group-hover:text">Profil</a>
                <div class=" text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'berita' }">Berita</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'sejarah' }">Sejarah Singkat</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'visimisi' }">Visi Misi Sasaran</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'manajemen' }">Manajemen</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'strukturorganisasi' }">Struktur Organisasi</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Akademik</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'departemen' }">Departemen</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programmagister' }">Program Magister</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programdoktor' }">Program Doktor</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'programprofesi' }">Program Profesi</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'akreditasi' }">Akreditasi</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'kalenderakademik' }">Kalender Akademik</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Sumber Daya</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'gurubesar' }">Guru Besar</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'tenagakependidikan' }">Tenaga Kependidikan</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'saranadanprasarana' }">Sarana dan Prasarana</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'perpustakaan' }">Perpustakaan</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">K3</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'profilk3' }">Profil K3</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'strukturorganisasik3' }">Struktur Organisasi K3</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'tentangk3' }">Tentang K3 FT-UH</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'filependukung' }">File Pendukung</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Kemahasiswaan</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'asrama' }">UPT Asrama (RAMTEK)</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'pengembangankarakter' }">Pengembangan Karakter Mahasiswa</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'pengembanganprestasi' }">Peningkatan Prestasi Mahasiswa</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'inbound' }">Mahasiswa Inbound dan Outbound</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'alumni' }">Alumni</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'aturankemahasiswaan' }">Aturan Kemahasiswaan</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'pengumuman' }">Pengumuman</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Riset dan Informasi</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'daftarpenelitian' }">Daftar Penelitian LBE Tahun 2020</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'hasilinovasi' }">Hasil Inovasi</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'hakkekayaan' }">Hak Kekayaan Intelektual</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Kemitraan</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'kerjasamadalamnegeri' }">Kerjasama Dalam Negeri</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'kerjasamaluarnegeri' }">Kerjasama Luar Negeri</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">GPM-PR</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'profilgpm' }">Profil GPM-PR</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'dokumenmutu' }">Dokumen Mutu</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'auditmutu' }">Audit Mutu Akademik Internal</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'lamteknik' }">LAM Teknik</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'surveikepuasanpengguna' }">Survei Kepuasan Pengguna</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'surveimahasiswa' }">Survei Kepuasan Layanan Mahasiswa</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'galeri' }">Galeri</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">COT</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'cotweb' }">Cot Website</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'jurnalcot' }">Jurnal COT</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'cotnewsletter' }">COT Newsletter</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'uigcollaboration' }">U-I-G COLLABORATION</NuxtLink></p>
                </div>
            </div>
            <p class="text-2xl">|</p>
            <div class="relative group pt-1">
                <a href="#" class="px-5 hover:text-amber-600 group-hover:text">Dharma Wanita</a>
                <div class="text-left absolute hidden bg-white text-black/50 group-hover:block w-max px-5 py-2 rounded shadow-lg fixed" style="background-color: white">
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'halamanutamadharmawanita' }">Halaman Utama Dharma Wanita</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'strukturorganisasidharmawanita' }">Struktur Organisasi Dharma Wanita</NuxtLink></p>
                    <p class="py-2 hover:bg-black/10 px-1"><NuxtLink :to="{ name: 'kegiatandharmawanita' }">Kegiatan Dharma Wanita</NuxtLink></p>
                </div>
            </div>
          </li>
        </ul>
      </nav>
    </div>
  </header>
  <!-- navbar end -->
</template>