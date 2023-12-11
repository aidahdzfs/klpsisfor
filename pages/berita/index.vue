<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] h-[201px] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Berita</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

    <!-- berita start -->
    <section class="ml-28 px-16 my-10">
      <div>
        <h1 class="text-black text-3xl font-bold pb-2">BERITA</h1>
        <img src="../assets/image/line.png" class="w-56 h-1">
      </div>
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
    </section>
    <!-- berita end -->
    </main>

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