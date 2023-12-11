<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Home Page Dharma Wanita</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="px-16 m-20">
            <div class="mb-10 relative">
                <h1 class="text-black text-3xl font-bold pb-2 text-center">PENGURUS DHARMA WANITA FTUH 2022/2026</h1>
                <img src="../assets/image/Rectangle19.png" class="place-self-center relative m-auto">
            </div>
            <div class="bg-[url('/assets/image/dharma.jpg')] flex p-10 justify-center m-auto items-center gap-x-20">
                <div class="">
                    <img src="../assets/image/wanita.png" alt="error" class="w-96 h-60">
                </div>
                <div class="">
                    <p class="text-white">
                        Ny. Muralia Isran Ramli (Ketua) <br>
                        Ny. Sri Muliani Amil Ilham (Wakil Ketua I) <br>
                        Ny. Fauziah Rusman (Wakil Ketua II) <br>
                        Ny. Syafriani Rustan Tarakka (Wakil Ketua III) <br>
                        Ny. Hafny Mufti Radja (Sekretaris) <br>
                        Ny. Harsini Mukti Ali (Bendahara) <br>
                        Ny. Diah Purnawa Niswar (Wakil Sekretaris I) <br>
                        Ny. Seilah Akbar Caronge (Wakil Sekretaris II) <br>
                        Ny. A. Nurfaidah Jalaluddin (Wkl Sekretaris III) <br>
                        Ny. Tyanita P. Zulkifly Tahir (Wakil Bendahara I) <br>
                        Ny. Asra Chairul Paotonan (Wakil Bendahara II) <br>
                        Ny. Fatmawati Hairul Arsyad (Wk Bendahara III)
                    </p>
                </div>
            </div>
            <div class="my-20 relative">
                <h1 class="text-black text-3xl font-bold pb-2 text-center">GALERI DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class="place-self-center relative m-auto">
            </div>
            <div class="my-20 relative">
                <h1 class="text-black text-3xl font-bold pb-2 text-center">BERITA DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class="place-self-center relative m-auto">
            </div>
        </section>

    <!-- dharma wanita start -->
        <!-- <div class="bg-[url('/assets/image/dharma.jpg')] flex p-10 pr-20">
            <div class="w-1/3 pr-10">
                <img src="../assets/image/wanita.png" alt="error" class="w-96 h-60">
            </div>
            <div class="w-2/3">
                <h1 class="text-white font-bold tracking-widest pb-3">DHARMA WANITA</h1>
                <img src="../assets/image/line.png" alt="error" class="w-52 h-[2px]">
                <p class="text-white text-justify pt-10 pb-6">Dharma Wanita Persatuan Fakultas Teknik Unhas yang diketuai oleh Ny. Muralia Isran Ramli, aktif melakukan berbagai macam kegiatan seperti amaliah ramadhan, arisan di kapal, kegiatan BKMT dan DPW Unhas.</p>
                <button class="rounded-3xl border-2 px-7 pb-[8px] pt-[10px] text-sm font-medium text-neutral-50 duration-150 ease-in-out hover:border-neutral-100 hover:bg-neutral-500 hover:bg-opacity-10 hover:text-neutral-100 focus:border-neutral-100 focus:text-neutral-100 focus:outline-none focus:ring-0 active:border-neutral-200 active:text-neutral-200 dark:hover:bg-neutral-100 dark:hover:bg-opacity-10"
                    data-te-ripple-init
                data-te-ripple-color="light">SELENGKAPNYA</button>
            </div>
        </div> -->
    <!-- <div class="text-center pt-20 ">
        <h1 class="text-black text-3xl font-bold pb-2">GALERI DHARMA WANITA</h1>
        <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
        <div id="kalender" class=" space-x-10 items-center text-center grid grid-cols-3 relative justify-center">
            <div v-for="item in halamanutamadharmawanitaData" :key="item.id">
                <div class="mt-10 mb-4">
                <img :src="getImageUrl(item.gambar)" :alt="`galeri ${item.id}`" class="relative m-auto" style="width: 350px; height: 200px; margin-bottom: 20px; margin-top: 10px;"/>
            </div>
            <div style="margin-bottom: 20px;">
                <h1 class="font-bold text-center" style="font-size: 18px;" v-html="item.judul"></h1>
            </div>
    </div>
            <div class="text-center pt-20 ">
                <h1 class="text-black text-3xl font-bold pb-2">BERITA DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
            </div>
            <div class="text-center pt-20 ">
                <h1 class="text-black text-3xl font-bold pb-2">VIDEO DHARMA WANITA</h1>
                <img src="../assets/image/Rectangle19.png" class=" mx-[550px]">
            </div>
        </section> -->
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/halamanutamadharmawanita"
    const halamanutamadharmawanitaData = ref('');

    async function getHalamanutamadharmawanita() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        halamanutamadharmawanitaData.value = data.data
    }

    onMounted(() => {
        getHalamanutamadharmawanita();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>