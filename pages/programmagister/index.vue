<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Program Magister</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="py-8 my-10">
            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">PROGRAM MAGISTER</h1>
                <img src="../assets/image/Rectangle19.png" class="ml-100">
            </div>
            <div v-for="item in magisterData" :key="item.id" class="w-[100vw] text-black text-lg font-medium text-justify justify-center ml-28 mt-10 pr-56">
                <p class="font-medium" v-html="item.isi"></p>
            </div>
        </section>
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/magister"
    const magisterData = ref('');

    async function getMagister() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        magisterData.value = data.data
    }

    onMounted(() => {
        getMagister();
    })

</script>