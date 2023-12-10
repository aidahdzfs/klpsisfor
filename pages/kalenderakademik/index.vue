<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Kalender Akademik</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8 ml-28">

            <!-- <div id="kalender">
                <div v-for="item in kalenderData" :key="item.id">
                    <div class="flex flex-row">
                        <img :src="getImageUrl(item.gambar)" :alt="`kalender ${item.id}`" class=" max-w-xl mr-10">
                    </div>
                </div>

            </div> -->
            <div class="">
                <h1 class="text-black text-3xl font-bold pb-2">Kalender Akademik</h1>
                <img src="../assets/image/Rectangle19.png" class="mb-10">
            </div>
            <div class="flex items-center justify-center">
                <img src="../assets/image/kalenderakademik.png" alt="kalenderakademik" class="max-w-xl mr-10">
                <img src="../assets/image/kalenderakademik2.jpg" alt="kalenderakademik" class="max-w-xl">
            </div>
        </section>
    </main>
</template>


<!-- <script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/kalender"
    const kalenderData = ref([]);

    async function getKalender() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        kalenderData.value = data.data
    }

    onMounted(() => {
        getKalender();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script> -->