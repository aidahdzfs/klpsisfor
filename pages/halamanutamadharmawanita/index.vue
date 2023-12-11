<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-medium">Home Page Dharma Wanita</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-medium">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-medium">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="mt-10 py-8">
            <div id="sejarah">
                <div >

                </div>

            </div>
            <div class="text-center ">
                <h1 class="text-black text-3xl font-bold pb-2">PENGURUS DHARMA WANITA FT-UH 2022/2026</h1>
                <img src="../assets/image/Rectangle20.png" class=" mx-64">
            </div>
            <div class="text-center pt-20 ">
                <h1 class="text-black text-3xl font-bold pb-2">GALERI DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
            </div>
            <div class="text-center pt-20 ">
                <h1 class="text-black text-3xl font-bold pb-2">BERITA DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
            </div>
            <div class="text-center pt-20 ">
                <h1 class="text-black text-3xl font-bold pb-2">VIDEO DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/sejarah"
    const sejarahData = ref('');

    async function getSejarah() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        sejarahData.value = data.data
    }

    onMounted(() => {
        getSejarah();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>