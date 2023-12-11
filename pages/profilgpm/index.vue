<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Profil GPM-PR</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 text-lg ml-28 py-8 pr-[155px]">
            <div class=" my-5 text-justify leading-relaxed">
                <h1 class="text-black text-3xl font-bold pb-2">PROFIL GPM-PR</h1>
                <img src="../assets/image/Rectangle19.png" class="w-72 h-1">
            </div>
            <div class="text-justify leading-relaxed mt-10">
                <h3 class="font-bold">TUGAS DAN FUNGSI</h3>
                <p class="mt-4">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gugus Penjaminan Mutu dan Peningkatan Reputasi (GPM-PR) adalah Gugus yang dibentuk oleh Rektor 
                    dengan tugas melakukan penjaminan dan pengendalian mutu internal di tingkat Fakultas. GPM mempunyai tugas merencanakan, menerapkan, 
                    mengendalikan dan mengembangkan sistem penjaminan mutu akademik fakultas dan program studi yang sejalan dengan sistem penjaminan mutu internal 
                    Unhas, dan bertanggungjawab atas peningkatan mutu secara berencana dan berkelanjutan. Dalam menjalankan Tupoksinya, GPM dibantu pula oleh Unit 
                    Penjaminan Mutu di tingkat Prodi/Profesi.<br><br>Dalam melaksanakan tugasnya, GPM-PR mempunyai fungsi :</p>
                <ul class="list-outside list-decimal ml-10 text-left space-y-3 mt-4">
                    <li>Perumusan kebijakan mutu akademik yang sejalan dengan kebijakan mutu akademik Unhas, dalam rangka pencapaian target kinerja akademik fakultas dan program studi</li>
                    <li>Perumusan dan pengembangan standar mutu akademik yang sejalan dengan standar mutu Unhas</li>
                    <li>Pelaksanaan standar mutu akademik dan manajemen yang sejalan dengan standar mutu Unhas</li>
                    <li>Perumusan manual mutu akademik yang sejalan dengan manual mutu Unhas</li>
                    <li>Pengembangan sistem monitoring dan evaluasi mutu akademik berbasis sistem informasi</li>
                    <li>Pelaksanaan monitoring dan evaluasi kegiatan jaminan mutu akademik</li>
                    <li>penyampaian laporan hasil monitoring dan evaluasi beserta rekomendasinya secara tertulis kepada Dekan</li>
                    <li>Pelaksanaan analisis terhadap tindak lanjut pelaksanaan monitoring dan evaluasi</li>
                    <li>Pemberian rekomendasi perbaikan untuk mencapai sasaran fakultas dan program studi</li>
                    <li>Pelaksanaan tugas lain yang diberikan oleh dekan</li>
                </ul>
            </div>
            <div class="text-justify leading-relaxed">
                <h3 class="font-bold mt-8 mb-2">PELAKSANA TUGAS</h3>
                <div id="profil gpm" class="flex items-center justify-center space-x-40">
                    <div v-for="item in profilgpmData" :key="item.id" class=" ">
                        <img :src="getImageUrl(item.gambar)" :alt="`profilgpm ${item.id}`" class="mt-10 mb-4 h-48 w-44 relative m-auto"/>
                        <h1 v-html="item.judul" class=" font-bold text-base"></h1>
                        <p v-html="item.isi" class=" text-sm text-center"></p>
                    </div>
                </div>
            </div>
            <div class="text-justify leading-relaxed">
                <h3 class="font-bold mt-8 mb-2">REFERENSI</h3>
                <ul class="list-outside list-decimal text-justify ml-10 space-y-2 mt-4">
                    <li>PERATURAN SENAT AKADEMIK UNIVERSITAS HASANUDDIN NOMOR:4867/UN4.2/IT.03/2017 TENTANG KEBIJAKAN SISTEM PENJAMINAN MUTU INTERNAL UNIVERSITAS HASANUDDIN</li>
                    <li>PERATURAN REKTOR UNIVERSITAS HASANUDDIN NOMOR 8/UN4.1/2018 TENTANG ORGANISASI DAN TATA KERJA PENGELOLA UNIVERSITAS HASANUDDIN</li>
                    <li>PERATURAN REKTOR UNIVERSITAS HASANUDDIN NOMOR 10/UN4.1/2018 TENTANG ORGANISASI DAN TATA KERJA LEMBAGA DAN SATUAN UNIVERSITAS HASANUDDIN</li>
                    <li>PERATURAN REKTOR UNIVERSITAS HASANUDDIN NOMOR 13/UN4.1/2018 TENTANG ORGANISASI DAN TATA KERJA FAKULTAS DAN SEKOLAH UNIVERSITAS HASANUDDIN</li>
                    <li>PERATURAN REKTOR UNIVERSITAS HASANUDDIN NOMOR 2/UN4.1/2022 TENTANG ORGANISASI DAN TATA KERJA PENGELOLA UNIVERSITAS HASANUDDIN</li>
                </ul>
            </div>
        </section>
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/profilgpm"
    const profilgpmData = ref([]);

    async function getProfilgpm() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        profilgpmData.value = data.data
    }

    onMounted(() => {
        getProfilgpm();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
}
</script>