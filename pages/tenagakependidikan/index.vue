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
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-white hover:bg-white border border-gray bg-amber-600 dark:border-gray dark:hover:text-zinc-700">1</a>
                    </li>
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white"><NuxtLink to="/tenagakependidikan2">2</NuxtLink></a>
                    </li>
                    <li>
                        <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray rounded-e-lg hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">Next</a>
                    </li>
                </ul>
            </div>


        <!-- table -->
        <!-- <div class="relative overflow-x-auto shadow-md sm:rounded-lg mx-40 my-20">
            <table class="w-full text-lg text-center rtl:text-right text-gray-500 dark:text-gray-400">
                <thead class="text-xl text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
                    <tr>
                        <th scope="col" class="px-6 py-3">
                            No
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Nama
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Jabatan
                        </th>
                        <th scope="col" class="px-6 py-3">
                            NIP
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Golongan
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="odd:bg-white odd:dark:bg-zinc-300">
                        <td class="px-6 py-4">
                            1
                        </td>
                        <td class="px-6 py-4">
                            Rosnah S.HUM
                        </td>
                        <td class="px-6 py-4">
                            Pustakawan
                        </td>
                        <td class="px-6 py-4">
                            196102041986092001
                        </td>
                        <td class="px-6 py-4">
                            IVc
                        </td>
                    </tr>

                    <tr class="odd:bg-white">
                        <td class="px-6 py-4">
                            2
                        </td>
                        <td class="px-6 py-4">
                            Ir. Jumadil, S.T., M.M.
                        </td>
                        <td class="px-6 py-4">
                            Kabag Tata Usaha
                        </td>
                        <td class="px-6 py-4">
                            197308031993031001
                        </td>
                        <td class="px-6 py-4">
                            IVa
                        </td>
                    </tr>

                    <tr class="odd:bg-white odd:dark:bg-zinc-300">
                        <td class="px-6 py-4">
                            3
                        </td>
                        <td class="px-6 py-4">
                            Kartiah Gani, SE., M.M.
                        </td>
                        <td class="px-6 py-4">
                            Kasubag Keuangan dan Kepegawaian
                        </td>
                        <td class="px-6 py-4">
                            196406211993032005
                        </td>
                        <td class="px-6 py-4">
                            IVa
                        </td>
                    </tr>

                    <tr class="odd:bg-white">
                        <td class="px-6 py-4">
                            4
                        </td>
                        <td class="px-6 py-4">
                            Suhana, S.Ag
                        </td>
                        <td class="px-6 py-4">
                            Staf Adminitrasi Akademik
                        </td>
                        <td class="px-6 py-4">
                            197207102007012002	
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white odd:dark:bg-zinc-300">
                        <td class="px-6 py-4">
                            5
                        </td>
                        <td class="px-6 py-4">
                            Amsal Salim, S.T.
                        </td>
                        <td class="px-6 py-4">
                            Laboran Departemen Teknik Elektro
                        </td>
                        <td class="px-6 py-4">
                            197009301991031003
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white">
                        <td class="px-6 py-4">
                            6
                        </td>
                        <td class="px-6 py-4">
                            Syarifuddin, S.T.
                        </td>
                        <td class="px-6 py-4">
                            Laboran Departemen Teknik Lingkungan
                        </td>
                        <td class="px-6 py-4">
                            196607301989031003	
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white odd:dark:bg-zinc-300">
                        <td class="px-6 py-4">
                            7
                        </td>
                        <td class="px-6 py-4">
                            Abd. Kadir A. Rahman, SE
                        </td>
                        <td class="px-6 py-4">
                            Kasubag Umum dan Perlengkapan
                        </td>
                        <td class="px-6 py-4">
                            197207182002121001
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white">
                        <td class="px-6 py-4">
                            8
                        </td>
                        <td class="px-6 py-4">
                            Ruddin, S. Sos
                        </td>
                        <td class="px-6 py-4">
                            Kordinator Lapangan
                        </td>
                        <td class="px-6 py-4">
                            196812311989031005
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white odd:dark:bg-zinc-300">
                        <td class="px-6 py-4">
                            9
                        </td>
                        <td class="px-6 py-4">
                            Hartika, S.E
                        </td>
                        <td class="px-6 py-4">
                            Staf Administrasi Departemen Teknik Elektro
                        </td>
                        <td class="px-6 py-4">
                            196904211995012001	
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>

                    <tr class="odd:bg-white">
                        <td class="px-6 py-4">
                            10
                        </td>
                        <td class="px-6 py-4">
                            Mustakim, S.T.
                        </td>
                        <td class="px-6 py-4">
                            Staf Administrasi Departemen Teknik Elektro
                        </td>
                        <td class="px-6 py-4">
                            197003221991031003	
                        </td>
                        <td class="px-6 py-4">
                            IIId
                        </td>
                    </tr>
                </tbody>
            </table> -->

            



        <!-- </div>
        <ul class="flex space-x-5 text-lg font-bold justify-center items-center">
            <li>
                <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray rounded-s-lg hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">Prev</a>
            </li>
            <li>
                <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white active:bg-amber-600">1</a>
            </li>
            <li>
                <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">2</a>
            </li>
            <li>
                <a href="#" class="flex items-center justify-center px-6 h-12 text-zinc-700 bg-white border border-gray rounded-e-lg hover:bg-amber-600 dark:bg-white dark:border-gray dark:hover:text-white">Next</a>
            </li>
        </ul> -->
        </section>
    </main>
</template>

<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/tenagaKependidikan"
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