<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl semibold">Dokumen Mutu</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8 mr-[155px] ml-28">
            <div>
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">DOKUMEN MUTU</h1>
                    <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
                </div>
                <ul class="list-outside list-disc text-justify ml-10 space-y-2 mb-10 mt-4">
                    <li class="font-bold text-lg mt-10">KEBIJAKAN SPMI</li>
                    <div id="dokumenmutu">
                        <div v-for="item in dokumenmutuData" :key="item.id">
                            <div class="flex space-x-10 items-center">
                                <img :src="getImageUrl(item.gambar)" :alt="`kebijakanSPMI ${item.id}`" class="max-w-[10rem]"/>
                                <p v-html="item.isi"></p>
                            </div>
                        </div>
                    </div>
                    <li class="font-bold text-lg pt-5">MANUAL SPMI</li>
                    <div v-for="item in dokumenmutuData" :key="item.id">
                        <div class="flex space-x-10 items-center">
                            <img :src="getImageUrl(item.gambar2)" :alt="`kebijakanSPMI ${item.id}`" class="max-w-[10rem]"/>
                            <p v-html="item.isi2"></p>
                        </div>
                    </div>
                    <li class="font-bold text-lg pt-5">STANDAR SPMI</li>
                    <div v-for="item in dokumenmutuData" :key="item.id">
                        <div class="flex space-x-10 items-center">
                            <img :src="getImageUrl(item.gambar3)" :alt="`kebijakanSPMI ${item.id}`" class="max-w-[10rem]"/>
                            <p v-html="item.isi3"></p>
                        </div>
                    </div>
                    <li class="font-bold text-lg pt-5">FORMULIR SPMI</li>
                    <div v-for="item in dokumenmutuData" :key="item.id">
                        <div class="flex space-x-10 items-center">
                            <img :src="getImageUrl(item.gambar3)" :alt="`kebijakanSPMI ${item.id}`" class="max-w-[10rem]"/>
                            <p v-html="item.isi3"></p>
                        </div>
                    </div>
                </ul>
                <p class="font-black text-center">Standar Mutu Unhas dan Indikatornya dapat di unduh di link berikut : <span><a href="https://docs.google.com/spreadsheets/d/1rtyW3caP9OKibK4H67g5VjoUmvQhoGXl/edit?rtpof=true&sd=true#gid=2063511492" class="text-sky-700 font-semibold hover:text-navy">STANDAR UNHAS</a></span></p>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/dokumenmutu"
    const dokumenmutuData = ref('');

    async function getDokumenmutu() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        dokumenmutuData.value = data.data
    }

    onMounted(() => {
        getDokumenmutu();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>