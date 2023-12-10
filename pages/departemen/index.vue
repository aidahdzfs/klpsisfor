<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[44px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Departemen</a>
                    <a href="#" class="w-[180px] h-[44px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[44px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>
        </section>
        <!-- header end -->

        <section class="my-10 py-8">
            <div class="ml-28">
                <h1 class="text-black text-3xl font-bold pb-2">DEPARTEMEN FT-UH</h1>
                <img src="../assets/image/Rectangle19.png" class="ml-100">
            </div>
            <div v-for="item in departemenData" :key="item.id" class="ml-28 mt-5 mb-20 pr-56 text-base">
                <div>
                    <a href="https://civil.unhas.ac.id/" class="text-sky-700 hover:text-navy">1. Departemen Teknik Sipil</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Sipil (Akreditasi Unggul BAN-PT, Akreditasi Internasional IABEE, Akreditasi Internasional ABET, Sertifikat AUN-QA)</li>
                        <li>Program Magister Teknik Sipil (Akreditasi A BAN-PT)</li>
                        <li>Program Doktor Teknik Mesin (Akreditasi B BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/mesin" class="text-sky-700 hover:text-navy">2. Departemen Teknik Mesin</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Mesin (Akreditasi Unggul BAN-PT, Akreditasi Internasional ASIIN)</li>
                        <li>Program Magister Teknik Mesin (Akreditasi Unggul LAMTEK)</li>
                        <li>Program Doktor Ilmu Teknik Sipil (Akreditasi Unggul BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://nasp.unhas.ac.id/" class="text-sky-700 hover:text-navy">3. Departemen Teknik Perkapalan</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Perkapalan (Akreditasi Unggul LAMTEK, Akreditasi Internasional ASIIN)</li>
                        <li>Program Magister Teknik Perkapalan (Akreditasi B BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/electrical/" class="text-sky-700 hover:text-navy">4. Departemen Teknik Elektro</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Elektro (Akreditasi Unggul LAMTEK, Akreditasi Internasional IABEE, Akreditasi Internasional ABET)</li>
                        <li>Program Magister Teknik Elektro (Akreditasi Unggul LAMTEK)</li>
                        <li>Program Doktor Teknik Elektro (Akreditasi B BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/architecture/id" class="text-sky-700 hover:text-navy">5. Departemen Teknik Arsitektur</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Arsitektur (Akreditasi Unggul BAN-PT, Sertifikat AUN-QA)</li>
                        <li>Program Magister Arsitektur (Akreditasi B BAN-PT)</li>
                        <li>Program Doktor Ilmu Arsitektur (Akreditasi A BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/geology/" class="text-sky-700 hover:text-navy">6. Departemen Teknik Geologi</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Geologi (Akreditasi Unggul BAN-PT, Sertifikat AUN-QA)</li>
                        <li>Program Magister Geologi (Akreditasi B BAN-PT)</li>
                        <li>Program Doktor Teknologi Kebumian dan Lingkungan (Akreditasi B BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/industri/" class="text-sky-700 hover:text-navy">7. Departemen Teknik Industri</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Industri (Akreditasi A BAN-PT, Akreditasi Internasional ASIIN)</li>
                        <li>Program Magister Teknik Industri (Akreditasi Baik BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://oceanengineering.unhas.ac.id/" class="text-sky-700 hover:text-navy">8. Departemen Teknik kelautan</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Kelautan (Akreditasi Unggul BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/tsp/" class="text-sky-700 hover:text-navy">9. Departemen Teknik Sistem Perkapalan</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Sistem Perkapalan (Akreditasi Unggul BAN-PT, Akreditasi Internasional ASIIN)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/pwk/id" class="text-sky-700 hover:text-navy">10. Departemen Teknik Perencanaan Wilayah Kota</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Perencanaan Wilayah dan Kota (Akreditasi A BAN-PT, Akreditasi Internasional ASIIN)</li>
                        <li>Program Magister Perencanaan Wilayah dan Kota (Akreditasi Baik BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/pertambangan/" class="text-sky-700 hover:text-navy">11. Departemen Teknik Pertambangan</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Pertambangan (Akreditasi A BAN-PT, Akreditasi Internasional ASIIN)</li>
                        <li>Program Magister Teknik Pertambangan (Akreditasi Baik BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://eng.unhas.ac.id/informatics/en" class="text-sky-700 hover:text-navy">12. Departemen Teknik Informatika</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Informatika (Akreditasi Unggul BAN-PT:, Akreditasi Internasional: ASIIN)</li>
                        <li>Program Magister Teknik Informatika (Akreditasi Baik Sekali BAN-PT)</li>
                    </ul>
                </div> 
                <div>
                    <a href="https://env.unhas.ac.id/" class="text-sky-700 hover:text-navy">13. Departemen Teknik Lingkungan</a>
                    <ul class="list-outside list-disc ml-8 mb-4">
                        <li>Program Sarjana Teknik Lingkungan (Akreditasi Unggul BAN-PT, Akreditasi Internasional IABEE)</li>
                        <li>Program Magister Teknik Lingkungan (Akreditasi Baik Sekali BAN-PT)</li>
                    </ul>
                </div>
                <!-- <div v-for="item in departemenData" :key="item.id" class="ml-28 mt-5 mb-20 pr-56 text-base">
                <div>
                    <p v-html="item.dept"></p>
                </div>
            </div> -->
            </div>
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/departemen"
    const departemenData = ref('');

    async function getDepartemen() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        departemenData.value = data.data
    }

    onMounted(() => {
        getDepartemen();
    })

</script>