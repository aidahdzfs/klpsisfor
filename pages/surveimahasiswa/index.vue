<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl semibold">Survei Kepuasan Layanan Mahasiswa</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8 mr-[155px] ml-28">
            <div class="text-lg">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">INSTRUMEN SURVEI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-96 h-1">
                </div>
                <div class="text-justify leading-relaxed mt-10">
                    <div id="surveimahasiswa">
                        <div v-for="item in surveiMahasiswaData" :key="item.id">
                            <div style="margin-bottom: 20px;">
                                <p v-html="item.isi"></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/surveimahasiswa"
    const surveiMahasiswaData = ref('');

    async function getSurveiMahasiswa() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        surveiMahasiswaData.value = data.data
    }

    onMounted(() => {
        getSurveiMahasiswa();
    })
</script>