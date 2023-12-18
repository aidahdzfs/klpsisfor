<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl semibold">Visi, Misi dan Sasaran</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8">
            <!-- Visi -->
            <div>
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">VISI</h1>
                    <img src="../assets/image/line.png" class="w-48 h-1">
                </div>
                <div v-for="item in visimisiData" :key="item.id">
                <p v-html="item.visi"></p>
            </div>
            </div>
            <!-- Visi end -->
            
            <!-- Misi -->
            <div class="mt-20">
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">MISI</h1>
                    <img src="../assets/image/Rectangle18.png" class="w-48 h-1">
                </div>
                <div v-for="item in visimisiData" :key="item.id">
                    <p v-html="item.misi"></p>
                </div>
            </div>
            <!-- Misi end -->

            <!-- Sasaran -->
            <div class="mt-20">
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">SASARAN</h1>
                <img src="../assets/image/Rectangle18.png" class="w-48 h-1">
                </div>
                <div v-for="item in visimisiData" :key="item.id">
                    <p v-html="item.sasaran"></p>
                </div>
            </div>
            <!-- Sasaran end -->
        </section>
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/visimisi"
    const visimisiData = ref('');

    async function getVisimisi() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        visimisiData.value = data.data
    }

    onMounted(() => {
        getVisimisi();
    })
</script>
