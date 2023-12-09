<template>
    <!-- galeri start -->
    <section class="px-16">
      <h1 class="text-3xl font-bold">GALERI</h1>
      <img src="../assets/image/line.png" alt="error" class="pt-2">
      <div class = "flex px-20 gap-4">
        <div>
          <img src="../assets/image/panah1.png" alt="error" class="py-14 px-3 my-10 cursor-pointer">
        </div>
        <div>
          <img src="../assets/image/galeri1.png" alt="error" class="py-6 mx-3 cursor-pointer">
          <h1 class="text-center font-bold cursor-pointer hover:text-amber-600">Rapat Kerja Fakultas Teknik</h1>
        </div>
        <div>
          <img src="../assets/image/galeri2.png" alt="error" class="py-6 mx-3 cursor-pointer">
          <h1 class="text-center font-bold cursor-pointer hover:text-amber-600">Pengabdian Masyarakat</h1>
        </div>
        <div>
          <img src="../assets/image/galeri3.png" alt="error" class="py-6 mx-3 cursor-pointer">
          <h1 class="text-center font-bold cursor-pointer hover:text-amber-600">Pelantikan dan Pengabdian Sumpah Jabatan Pejabat</h1>
        </div>
        <div>
          <img src="../assets/image/panah2.png" alt="error" class="py-14 px-3 my-10 cursor-pointer">
        </div>
      </div>
      <img src="../assets/image/line2.png" alt="error" class="pt-10">
      <div v-for="item in galeriData" :key="item.id">
        <img :src="getImageUrl(item.image)" :alt="`galeri ${item.id}`" class="w-full">
      </div>
    </section>
    <!-- galeri end -->
</template>

<script setup>
  import { ref, computed, onMounted } from 'vue';

const endpoint = "http://localhost:8055/items/galeri"
const galeriData = ref([]);

async function getGaleri() {
  const api = await fetch(endpoint)
  const data = await api.json()
  console.log(data.data)
  galeriData.value = data.data;
}

onMounted(() => {
  getGaleri();
})


const getImageUrl = (imageName) => {
  return `http://localhost:8055/assets/${imageName}`;
};
 
</script>
