<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] h-[201px] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">File Pendukung</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8 ml-28">
            <!-- sop -->
            <div>
                <div>
                    <h1 class="text-black text-3xl font-bold">SOP KESEHATAN KERJA FT-UH</h1>
                    <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
                </div>
                <div id="filePendukung">
                    <div v-for="item in filePendukungData" :key="item.id">
                        <div class="pt-8">
                            <p v-html="item.isi"></p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- sop end -->

            <!-- form start -->
            <div>
                <div>
                    <h1 class="text-black text-3xl font-bold pt-1">FORM K3</h1>
                    <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
                </div>
                <div id="filePendukung">
                    <div v-for="item in filePendukungData" :key="item.id">
                        <div class="pt-8">
                            <p v-html="item.isi2"></p>
                        </div>
                    </div>
                </div>
            </div>
            <!-- form end -->
        </section>
    </main>

</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/filependukung"
    const filePendukungData = ref('');

    async function getFilePendukung() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        filePendukungData.value = data.data
    }

    onMounted(() => {
        getFilePendukung();
    })
</script>