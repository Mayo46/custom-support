<script setup>
import {RouterView } from 'vue-router'
import Navbar from '@/layouts/Navbar.vue'
import Footer from '@/layouts/Footer.vue'
components:{
  Navbar,
  Footer
}
</script>

<template>
    <Navbar/>
    <router-view/>
    <Footer/>
</template>