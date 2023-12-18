<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl semibold">Audit Mutu Akademik Internal</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 text-lg py-8 mr-[155px] ml-28">
            <div>
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">AUDIT MUTU AKADEMIK INTERNAL (AMAI) FT-UH</h1>
                    <img src="../assets/image/Rectangle19.png">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">SISTEM MUTU</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-72 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi2"></p>
                        </div>
                        <div class="flex items-center justify-center">
                            <img :src="getImageUrl(item.gambar2)" :alt="`auditMutu ${item.id}`" class="mt-5 place-self-center relative m-auto w-[50rem] h-[20rem]"/>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">STANDAR MUTU AKADEMIK INTERNAL</h1>
                    <img src="../assets/image/Rectangle19.png">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi3"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">FUNGSI AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-60 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi4"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">TUJUAN AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-60 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi5"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">KARAKTERISTIK AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-96 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi6"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">LINGKUP AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-72 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi7"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">FOKUS AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-72 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi8"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">KEGIATAN AMAI</h1>
                    <img src="../assets/image/Rectangle19.png" class="w-72 h-1">
                </div>
                <div id="auditMutu">
                    <div v-for="item in auditMutuData" :key="item.id">
                        <div style="margin-bottom: 20px;">
                            <p v-html="item.isi9"></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-20">
                <div>
                    <h1 class="text-black text-3xl font-bold pb-2">SIKLUS SISTEM PEMINJAMAN MUTU</h1>
                    <img src="../assets/image/Rectangle19.png">
                </div>
                <div v-for="item in auditMutuData" :key="item.id">
                    <div style="margin-bottom: 20px;">
                        <p v-html="item.isi10"></p>
                    </div>
                    <div class="flex items-center justify-center">
                        <img :src="getImageUrl(item.gambar10)" :alt="`auditMutu ${item.id}`" class="mt-5 place-self-center relative m-auto w-[35rem]"/>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/auditmutu"
    const auditMutuData = ref('');

    async function getAuditMutu() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        auditMutuData.value = data.data
    }

    onMounted(() => {
        getAuditMutu();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>