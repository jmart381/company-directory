<template>
<div>

<button @click="prevPage" :disabled="activePage === 1">PREV</button>

<button v-for="page in pages" :key="page" class="">{{ page }}</button>

<button @click="nextPage" :disabled="activePage === pages">NEXT</button>

</div>

</template>

<script setup>
import { ref } from 'vue'
const pages = ref(10)
const active = ref(1)

const prevPage = () => {
    if (activePage.value > 1) {
        activePage.value--
    }
}
const nextPage = () => {
    if (activePage.value < pages.value) {
        activePage.value++
    }
 }



</script>