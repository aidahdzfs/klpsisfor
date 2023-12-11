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
            <div class="mt-10">
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">VISI</h1>
                    <img src="../assets/image/line.png" class="w-48 h-1">
                </div>
                <div class="w-[100vw] text-black text-lg font-medium text-justify justify-center ml-28 mt-6 mb-10 pr-56">Menjadi institusi unggulan dalam bidang rekayasa untuk keberlanjutan global dengan semangat budaya maritim.</div>
            </div>
            <!-- Visi end -->
            
            <!-- Misi -->
            <div class="mt-20">
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">MISI</h1>
                    <img src="../assets/image/Rectangle18.png" class="w-48 h-1">
                </div>
                <div class="w-[100vw] text-black text-lg font-medium text-justify justify-center ml-28 mt-6 mb-10 pr-56">
                    <ul class="list-outside list-disc ml-4 mb-4">
                        <li>Mengembangkan pendidikan, penelitian, dan pengabdian masyarakat pada bidang rekayasa dengan semangat budaya maritim.</li>
                        <li>Menghasilkan sarjana teknik yang berpengetahuan luas, menguasai teknologi maju dan berkemampuan inovasi.</li>
                        <li>Membangun pusat unggulan bidang rekayasa untuk pembangunan berkelanjutan</li>
                        <li>Menyebarluaskan teknologi tepat guna, peningkatan kualitas hidup, dan mempertahankan kelestarian sumber daya alam</li>
                    </ul>
                </div>
            </div>
            <!-- Misi end -->

            <!-- Sasaran -->
            <div class="mt-20">
                <div class="ml-28">
                    <h1 class="text-black text-3xl font-bold pb-2">SASARAN</h1>
                <img src="../assets/image/Rectangle18.png" class="w-48 h-1">
                </div>
                <div class="w-[100vw] text-black text-lg font-medium text-justify justify-center ml-28 mt-6 mb-10 pr-56">
                    <ul class="list-outside list-disc ml-4 mb-4">
                        <li>Membentuk keseimbangan penelitian – pendidikan; melalui keterpaduan sistem pendidikan yang komprehensif dan kreatif pada strata sarjana, dan percepatan penelitian pada strata pascasarjana melalui pendidikan berbasis laboratorium (Labo-Based Education / LBE).</li>
                        <li>Mengimplementasikan model pembelajaran LBE untuk pendidikan berorientasi penelitian.</li>
                        <li>Membangun jaringan kemitraan internasional untuk pendidikan dan penelitian.</li>
                        <li>Mengelola kegiatan pendidikan dan penelitian lintas disiplin ilmu.</li>
                        <li>Menghasilkan sarjana teknik yang memenuhi kriteria lulusan pendidikan keteknikan internasional.</li>
                        <li>Menghasilkan sarjana teknik dengan kompetensi sesuai dengan kebutuhan pasar kerja.</li>
                        <li>Menekankan pendidikan dan enelitian untuk pembangunan berkelanjutan bagi masyarakat global.</li>
                        <li>Mengintensifkan penelitian untuk pembangunan berkelanjutan di kawasan Indonesia Timur.</li>
                    </ul>
                    
                </div>
            </div>
            <!-- Sasaran end -->


            

            <!-- <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">VISI</h1>
                <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
            </div>
            <div v-for="item in visimisiData" :key="item.id">
                <p v-html="item.visi" class="px-28 pt-10"></p>
            </div>


            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">MISI</h1>
                <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
            </div>
            <div v-for="item in visimisiData" :key="item.id">
                <p v-html="item.misi" class="px-28 pt-10"></p>
            </div>


            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">SASARAN</h1>
                <img src="../assets/image/Rectangle18.png" class="ml-100 w-72 h-1">
            </div>
            <div v-for="item in visimisiData" :key="item.id">
                <ul class="list-outside list-disc ml-4 mb-4">
                    <li v-html="item.sasaran" class="px-28 pt-10"></li>
                </ul>
            </div> -->
        </section>
    </main>
</template>


<!-- <script setup>
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
</script> -->
