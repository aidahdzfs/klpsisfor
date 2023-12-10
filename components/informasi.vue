<template>
    <!-- informasi start -->
    <section class="px-16 mt-10">
      <h1 class="text-3xl font-bold">INFORMASI</h1>
      <img src="../assets/image/line.png" alt="error" class="pt-2">

      <div id="informasi" class="grid gap-15 grid-cols-2 py-8 pl-40">
        <div v-for="item in informasiData" :key="item.id" class="py-8">
          <h1 v-html="item.judul" class="text-sm max-w-lg cursor-pointer hover:text-amber-600"></h1>
          <div class="flex flex-row space-x-36 pt-10">
            <p class="flex text-gray"><img src="../assets/image/kalender.png" alt="error">{{ item.kalender }}</p>
          </div>
        </div>
      </div>
      <p class="text-blue text-sm text-center pt-16 cursor-pointer">Semua informasi>></p>
    </section>
    <!-- informasi end -->
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/informasi"
    const informasiData = ref('');

    async function getInformasi() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        informasiData.value = data.data
    }

    onMounted(() => {
        getInformasi();
    })
</script>