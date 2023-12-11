<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Tenaga Kependidikan</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8">
            <div id="tenagaKependidikan">
                <div v-for="item in tenagaKependidikanData" :key="item.id">
                    <div class="ml-28">
                        <h1 v-html="item.judul" class="text-black text-3xl font-bold pb-2"></h1>
                        <img src="../assets/image/Rectangle19.png" class="ml-100">
                    </div>
                    <div style="margin-bottom: 20px;">
                        <p class="font-medium text-justify px-28 pt-10" style="font-size: 20px;" v-html="item.isi"></p>
                    </div>
                </div>

                <!-- slider -->
                <ul class="flex space-x-5 text-lg font-bold justify-center items-center">
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray rounded-s-lg hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">Prev</a>
                    </li>
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white active:bg-amber-600"><NuxtLink to="/tenagakependidikan">1</NuxtLink></a>
                    </li>
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-white hover:bg-white border border-gray bg-amber-600 dark:border-gray dark:hover:text-zinc-700">2</a>
                    </li>
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray rounded-e-lg hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">Next</a>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/tenagaKependidikan1"
    const tenagaKependidikanData = ref([]);

    async function getTenagaKependidikan() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        tenagaKependidikanData.value = data.data
    }

    onMounted(() => {
        getTenagaKependidikan();
    })
</script>