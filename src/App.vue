<script setup>
import {RouterView } from 'vue-router'
import Navbar from '@/components/Navigation/Navbar.vue'
import Footer from '@/components/Navigation/Footer.vue'
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