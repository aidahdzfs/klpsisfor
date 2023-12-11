<template>
        <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Akreditasi</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8 mx-20">
            <div id="akreditasi">
                <div v-for="item in akreditasiData" :key="item.id">
                    <h1 class="text-black text-3xl font-bold pb-2" v-html="item.judul"></h1>
                    <img src="../assets/image/Rectangle19.png">

                    <div class="flex items-center justify-center py-20 mx-20 px-20" v-html="item.isi">
                    </div>
                </div>
                <div class="mb-10 ml-28">
                    <p>Sertifikat dan SK Akreditasi dapat diunduh melalui link berikut:</p>
                    <a href="https://drive.google.com/drive/folders/139BQ4DSVSioV6HBHJt40AFobDsM6Egka" class="font-semibold text-sky-700 hover:text-navy">SK Akreditasi FT 2020-2021</a>
                </div>
                
            </div>
        </section>


    </main>


</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/akreditasi"
    const akreditasiData = ref('');

    async function getAkreditasi() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        akreditasiData.value = data.data
    }

    onMounted(() => {
        getAkreditasi();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>