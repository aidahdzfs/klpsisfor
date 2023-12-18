<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Tentang K3 FT-UH</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 ml-28 py-8">
            <div >
                <h1 class="text-black text-3xl font-bold pb-2">TENTANG K3</h1>
                <img src="../assets/image/Rectangle19.png" class="w-60 h-1">
            </div>
            <div id="tentangk3">
                    <div v-for="item in tentangk3Data" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi"></p>
                        </div>
                    </div>
                </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/tentangk3"
    const tentangk3Data = ref('');

    async function getTentangk3() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        tentangk3Data.value = data.data
    }

    onMounted(() => {
        getTentangk3();
    })
</script>