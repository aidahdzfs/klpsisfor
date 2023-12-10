<template>
    <!-- berita start -->
    <section class="px-16 mt-10">
      <h1 class="text-3xl font-bold">BERITA</h1>
      <img src="../assets/image/line.png" alt="error" class="pt-2">
      <div id="berita" class="text-justify grid gap-24 grid-cols-2 pt-10 pr-40">
        <div v-for="item in berita1Data" :key="item.id">
          <div class="mt-4 mb-4">
            <img :src="getImageUrl(item.gambarBerita)" :alt="`berita ${item.id}`" class="relative m-auto" style="width: 100vw; height: 100%; margin-bottom: 20px; margin-top: 10px;"/>
            <div>
              <h1 class="font-bold max-w-lg cursor-pointer hover:text-amber-600" style="font-size: 15px; padding-right: 100px;" v-html="item.judulBerita">
              </h1>
            </div>
          </div>
          <div class="flex flex-row space-x-36 pt-10">
            <p class="flex text-gray"><img src="../assets/image/kalender.png" alt="error">{{ item.kalender }}</p>
            <p class="flex text-gray"><img src="../assets/image/profile.png" alt="error">{{ item.admin }}</p>
          </div>
          <img src="../assets/image/line3.png" alt="error" class="">
          <div>
            <p v-html="item.isiBerita"></p>
          </div>
        </div>
      </div>
      <p class="text-blue text-sm text-center pt-20 cursor-pointer">Lihat berita nasional yang lain>></p>
      <img src="../assets/image/line2.png" alt="error" class="pt-10">



       <!-- <h1 class="text-3xl font-bold">BERITA</h1>
      <img src="../assets/image/line.png" alt="error" class="pt-2">
      <div id="berita" class="grid gap-15 grid-cols-2 py-8">
        <div>
          <img src="../assets/image/berita1.png" alt="error">
          <h1 class="font-bold pt-5 max-w-lg cursor-pointer hover:text-amber-600">Fakultas Teknik Sukses Gelar Konferensi Internasional ICREST 2023</h1>
          <div class="flex pt-10">
            <div class="flex">
              <img src="../assets/image/kalender.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">13 Oktober 2023</p>
            </div>
            <div class="flex">
              <img src="../assets/image/profile.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">Admin FT-UH</p>
            </div>
          </div>
          <img src="../assets/image/line3.png" alt="error" class="py-2">
          <p class="max-w-lg text-justify text-sm">International Conference On Research In Engineering and Science Technology 2023 yang pertama sukses dilaksanakan oleh Fakultas Teknik Universitas Hasanuddin. Bertema Advanced Technologies to Fulfill SDGs For Suistainable Life, konferensi internasional ini digelar pada...</p>
        </div>
        <div>
          <img src="../assets/image/berita2.png" alt="error">
          <h1 class="font-bold pt-5 max-w-lg cursor-pointer hover:text-amber-600">Rapat Progress Pekerjaan II dengan Badan Penanggulangan Bencana Daerah Kab. Luwu Utara</h1>
          <div class="flex pt-10">
            <div class="flex">
              <img src="../assets/image/kalender.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">13 Oktober 2023</p>
            </div>
            <div class="flex">
              <img src="../assets/image/profile.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">Admin FT-UH</p>
            </div>
          </div>
          <img src="../assets/image/line3.png" alt="error" class="py-2">
          <p class="max-w-lg text-justify text-sm">Jumat, 23 September 2022 bertempat di Ruang Rapat Utama Puslantek-CoT lt.1 Gedung CoT, Kepala Pusat Unggulan Teknologi Center of Technology (PUSLANTEK-CoT) Fakultas Teknik Universitas Hasanuddin, Dr. Eng. Ir. Nasruddin, ST, MT menerima kunjungan dari...</p>
        </div>
        <div>
          <img src="../assets/image/berita3.png" alt="error" class="pt-14">
          <h1 class="font-bold pt-5 max-w-lg cursor-pointer hover:text-amber-600">Kedatangan Professor dari Jepang, Teknik Industri Fakultas Teknik Universitas Hasanuddin Laksanakan International Guest Lecturer</h1>
          <div class="flex pt-10">
            <div class="flex">
              <img src="../assets/image/kalender.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">11 Oktober 2023</p>
            </div>
            <div class="flex">
              <img src="../assets/image/profile.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">Admin FT-UH</p>
            </div>
          </div>
          <img src="../assets/image/line3.png" alt="error" class="py-2">
          <p class="max-w-lg text-justify text-sm">Departemen Teknik Industri Fakultas Teknik Universitas Hasanuddin menggelar International Guest Lecturer yang dibawakan oleh Profesor yang juga sebagai Head Of Laboratory Ergonomics for All Ages and Abilities dari Kyushu University Prof. Satoshi Muraki, Ph.D., CPE. International Guest Lecturer dilaksanakan pada...</p>
        </div>
        <div>
          <img src="../assets/image/berita4.png" alt="error" class="pt-14">
          <h1 class="font-bold pt-5 max-w-lg cursor-pointer hover:text-amber-600">Fakultas Teknik Universitas Hasanuddin Jadi Tuan Rumah Temu Ilmiah Ikatan Peneliti Lingkungan Binaan Indonesia ke - 11.</h1>
          <div class="flex pt-10">
            <div class="flex">
              <img src="../assets/image/kalender.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">11 Oktober 2023</p>
            </div>
            <div class="flex">
              <img src="../assets/image/profile.png" alt="error">
              <p class="text-[10px] text-gray pr-[25px]">Admin FT-UH</p>
            </div>
          </div>
          <img src="../assets/image/line3.png" alt="error" class="py-2">
          <p class="max-w-lg text-justif text-sm">Departemen Arsitektur Fakultas Teknik Universitas Hasanuddin terpilih menjadi pelaksana Temu Ilmiah Peneliti Lingkungan Binaan (IPLBI) yang Ke - 11. Temu Ilmiah ini dilaksanakan pada hari Kamis, 05 Oktober 2023 di Gedung CSA LT 1 Fakultas Teknik Universitas Hasanuddin, Gowa...</p>
        </div>
      </div>
      <p class="text-blue text-sm text-center pt-20 cursor-pointer">Lihat berita nasional yang lain>></p>
      <img src="../assets/image/line2.png" alt="error" class="pt-10"> -->
    </section>
    <!-- berita end -->
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/berita1"
    const berita1Data = ref('');

    async function getBerita1() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        berita1Data.value = data.data
    }

    onMounted(() => {
        getBerita1();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>