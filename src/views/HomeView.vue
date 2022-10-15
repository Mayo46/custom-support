<template>
<div>
  <Header />
  <Consumer />
</div>
</template>
<script setup>
import Header from "@/components/Header.vue";
import Consumer from "@/components/Consumer.vue";
components:{
  Header,Consumer
}
</script>