<template>
<div>
  <Header />
  <Consumer />
  <Stats />
  <Shipment />
</div>
</template>
<script setup>
import Header from "@/components/Header.vue";
import Consumer from "@/components/Consumer.vue";
import Stats from "@/components/Stats.vue";
import Shipment from "@/components/Shipment.vue";
components:{
  Header,Consumer,Stats,Shipment
}
</script>