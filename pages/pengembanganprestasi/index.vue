<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Peningkatan Prestasi Mahasiswa</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="mt-10 py-8">
            <div id="pengembanganprestasi">
                <div v-for="item in prestasiData" :key="item.id" class="pb-20">
                    <div class="ml-28 pb-10">
                        <h1 v-html="item.judul" class="text-black text-3xl font-bold pb-2"></h1>
                        <img src="../assets/image/line.png" class="ml-100">
                    </div>
                    <p class=" px-80 text-2xl" v-html="item.isi"></p>
                    <ol class="list-outside list-decimal ml-28 text-left space-y-3 text-lg pt-10">
                        <li v-html="item.isi1"></li>
                        <li v-html="item.isi2"></li>
                        <li v-html="item.isi3"></li>
                        <li v-html="item.isi4"></li>
                    </ol>
                    
                </div>
            </div>
                
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/pengembanganprestasi"
    const prestasiData = ref('');

    async function getPrestasi() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        prestasiData.value = data.data
    }

    onMounted(() => {
        getPrestasi();
    })
</script>