<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-medium">Sejarah Singkat</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-medium">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-medium">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="mt-10 py-8">
            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">SEJARAH SINGKAT</h1>
                <img src="../assets/image/Rectangle19.png" class="ml-100">
            </div>
            <div id="sejarah">
                <div v-for="item in sejarahData" :key="item.id">
                    <div style="margin-bottom: 20px;">
                        <p class="font-medium text-justify px-28 pt-10" style="font-size: 20px;" v-html="item.isi"></p>
                    </div>
                    <div class="flex items-center justify-center">
                        <img :src="getImageUrl(item.gambar)" :alt="`sejarah ${item.id}`" class="w-[850px] h-[450px] mt-10 mb-20"/>
                    </div>
                </div>
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