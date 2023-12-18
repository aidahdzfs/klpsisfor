<template>
    <main class="overflow-x-hidden">
        <!-- header -->
        <section class="pt-24">
            <div class="h-[202px] relative">
                <img class="w-[100%] left-0 top-2 absolute" src="../assets/image/jkcenterhlm.png" />
                <div class="w-[1439px] h-[201px] left-0 top-[1px] absolute bg-blue-400 bg-opacity-30"></div>
                <div class="w-[474px] h-[45px] relative top-20 left-20">
                    <a href="#" class="w-[302px] h-[45px] left-[172px] absolute text-slate-300 text-2xl font-semibold">Master Plan</a>
                    <a href="#" class="w-[172px] h-[45px] left-0 absolute text-center text-sky-950 text-2xl font-semibold">Halaman</a>
                    <a href="#" class="w-[180px] h-[45px] left-16 pt-1 absolute text-center text-sky-950 text-xl font-semibold">  > </a>
                </div>
            </div>

            <div id="masterplan" class="mx-28 my-20">
                <div v-for="item in masterplanData" :key="item.id">
                    <div class="mt-4 mb-4">
                        <p v-html="item.isi"></p>
                        <p class="flex text-gray">{{ item.master }}</p>
                    </div>  
                <div>      
                </div>
            </div>
            </div>
        </section>
        <!-- header end -->
    </main>
</template>


<script setup>
    import { ref, computed, onMounted } from "vue";

    const endpoint = "http://localhost:8055/items/masterplan"
    const masterplanData = ref('');

    async function getMasterplan() {
        const api = await fetch(endpoint)
        const data = await api.json()
        console.log(data.data)
        masterplanData.value = data.data
    }

    onMounted(() => {
        getMasterplan();
    })

    const getImageUrl = (imageName) => {
        return `http://localhost:8055/assets/${imageName}`
    }
</script>