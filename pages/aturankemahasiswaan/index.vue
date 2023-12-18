<template>
        <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Aturan Kemahasiswaan</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="ml-28 my-10 py-8">
            <div>
                <h1 class="text-black text-xl font-extrabold pb-5">Aturan Kemahasiswaan FT-UH</h1>
            </div>
            <div id="aturanKemahasiswaan" class="pr-[155px] text-justify leading-relaxed">
                <div v-for="item in aturanKemahasiswaanData" :key="item.id">
                    <div style="margin-bottom: 20px;">
                        <p class="text-left space-y-2 pr-[155px] text-lg" v-html="item.isi"></p>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/aturankemahasiswaan"
    const aturanKemahasiswaanData = ref('');

    async function getAturanKemahasiswaan() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        aturanKemahasiswaanData.value = data.data
    }

    onMounted(() => {
        getAturanKemahasiswaan();
    })
</script>