<template>
    <!-- galeri start -->
    <section class="px-16">
      <h1 class="text-3xl font-bold">GALERI</h1>
      <img src="../assets/image/line.png" alt="error" class="pt-2">

      <div class="max-w-screen-xl w-full bg-white overflow-hidden flex justify-center relative m-auto p-10">
          <div class="flex">
            <button @click="prevPage" :disabled="currentPage === 0" class="cursor-pointer mt-0">
              <img src="../assets/image/panah1.png" alt="error">
            </button>
            <div id="galeri" class="text-center grid grid-cols-3 relative justify-center"> 
              <div v-for="(item, index) in visibleItems" :key="item.id">
                <div class="mt-10 mb-4">
                  <img :src="getImageUrl(item.gambar)" :alt="`galeri ${item.id}`" class="relative m-auto" style="width: 350px; height: 200px; margin-bottom: 20px; margin-top: 10px;"/>
                </div>
                <div style="margin-bottom: 20px;">
                  <h1 class="font-bold text-center" style="font-size: 18px;" v-html="item.judul"></h1>
                </div>
              </div>
           </div>
           <button @click="nextPage" :disabled="currentPage === totalpages - 1" class="cursor-pointer">
                <img src="../assets/image/panah2.png" alt="error">
              </button>
        </div>
      </div>
      <img src="../assets/image/line2.png" alt="error" class="pt-10">
      
    </section>
    <!-- galeri end -->
</template>

<script setup>
  import { ref, computed, onMounted } from 'vue';

const endpoint = "http://localhost:8055/items/galeri"
const galeriData = ref([]);

const itemsPerPage = ref(3)
const currentPage = ref(0)
const totalpages = computed(() => Math.ceil(galeriData.value.length / itemsPerPage.value)
) 
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

const visibleItems = computed(() => {
  const start = currentPage.value * itemsPerPage.value;
  const end = start + itemsPerPage.value;
  return galeriData.value.slice(start, end);
});

const prevPage = () => {
  if (currentPage.value > 0){
    currentPage.value--;
  }
};

const nextPage = () => {
  if (currentPage.value < totalpages.value - 1) {
    currentPage.value++;
  }
};
 
</script>
