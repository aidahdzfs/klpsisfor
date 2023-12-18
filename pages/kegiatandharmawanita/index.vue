<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-medium">Daftar Kegiatan Dharma Wanita</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-medium">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-medium">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="mt-10 py-8">
            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">KEGIATAN DHARMA WANITA</h1>
                <img src="../assets/image/line.png" class="ml-100">
            </div>


            <div id="kegiatandharmawanita" class="text-justify pl-28 pt-10 pb-20 pr-96 grid gap-24 grid-cols-2">
                <div v-for="item in kegiatandharmawanitaData" :key="item.id">
                    <div class="mt-4 mb-4">
                        <img :src="getImageUrl(item.gambar)" :alt="`berita ${item.id}`" class="relative m-auto" style="width: 100vw; height: 100%; margin-bottom: 20px; margin-top: 10px;"/>
                        <div>
                        <h1 class="font-bold max-w-lg cursor-pointer hover:text-amber-600" style="font-size: 15px; padding-right: 100px;" v-html="item.judul">
                        </h1>
                        </div>
                    </div>
                    <div class="flex flex-row space-x-36 pt-10">
                        <p class="flex text-gray"><img src="../assets/image/kalender.png" alt="error">{{ item.kalender }}</p>
                        <p class="flex text-gray"><img src="../assets/image/profile.png" alt="error">{{ item.admin }}</p>
                    </div>
                    <img src="../assets/image/line3.png" alt="error" class="">
                    <div>
                        <p v-html="item.isikegiatan"></p>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/kegiatandharmawanita"
    const kegiatandharmawanitaData = ref('');

    async function getKegiatandharmawanita() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        kegiatandharmawanitaData.value = data.data
    }

    onMounted(() => {
        getKegiatandharmawanita();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>