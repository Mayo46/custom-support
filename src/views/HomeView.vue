<template>
<div>
  <Header />
  <Consumer />
  <Stats />
</div>
</template>
<script setup>
import Header from "@/components/Header.vue";
import Consumer from "@/components/Consumer.vue";
import Stats from "@/components/Stats.vue";
components:{
  Header,Stats
}
</script>