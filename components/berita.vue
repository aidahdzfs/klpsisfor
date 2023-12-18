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
      <p class="text-blue text-sm text-center pt-20 cursor-pointer"><NuxtLink to="/berita"> Lihat berita nasional yang lain>></NuxtLink></p>
      <img src="../assets/image/line2.png" alt="error" class="pt-10">
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