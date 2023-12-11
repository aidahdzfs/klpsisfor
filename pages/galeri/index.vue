<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Galeri</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8">
            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">GALERI</h1>
                <img src="../assets/image/Rectangle19.png">
            </div>
            <div id="kalender">
                <div v-for="item in galeri1Data" :key="item.id">
                    <div v-html="item.judul" class=" font-semibold text-2xl ml-28 pb-10 pt-20"></div>
                    <div class="flex space-x-10 items-center justify-center ">
                        <img :src="getImageUrl(item.gambar)" :alt="`galeri ${item.id}`" class="max-w-xl">
                        <img :src="getImageUrl(item.gambar2)" :alt="`galeri ${item.id}`" class="max-w-xl">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/galeri1"
    const galeri1Data = ref([]);

    async function getGaleri1() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        galeri1Data.value = data.data
    }

    onMounted(() => {
        getGaleri1();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>