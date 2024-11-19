<script setup>

import { ref, reactive } from 'vue'
import { db } from './data/guitarras'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue';
import Guitarra from './components/Guitarra.vue';

const guitarras = ref(db)

</script>

<template>

    <Header/>

    <main class="container-xl mt-5">
        
        <h2 class="text-center">Nuestra Colección</h2>

        <Guitarra
            v-for="guitarra in guitarras"
            :guitarra="guitarra"
            :key="guitarra.id"
        />

    </main>


    <Footer/>


</template>

<style scoped>

</style>
