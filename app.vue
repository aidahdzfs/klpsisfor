<script setup>
import Header from "./components/header.vue"
import Footer from "./components/footer.vue"


const { $directus, $readItems } = useNuxtApp()

const { data: global } = await useAsyncData('global', () => {
  return $directus.request($readItems('global'))
})
</script>

<template>
  <Header />
  <div>
    <NuxtPage />
  </div>
  <Footer />
</template>