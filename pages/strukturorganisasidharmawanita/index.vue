<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Struktur Organisasi Dharma Wanita</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class=" my-10 py-8">
            <div>
                <h1 class="text-black text-3xl font-bold pb-2 ml-28">STRUKTUR ORGANISASI DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class="ml-28">
            </div>
            <div v-for="item in strukturdharmaData" :key="item.id">
                <img :src="getImageUrl(item.gambar)" :alt="`struktur ${item.id}`" class="pt-16 pb-20 px-28">
            </div>
            
        </section>
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/strukturdharmawanita"
    const strukturdharmaData = ref('');

    async function getStrukturdharma() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        strukturdharmaData.value = data.data
    }

    onMounted(() => {
        getStrukturdharma();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>