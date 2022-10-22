<template>
<div>
  <Header />
  <Consumer />
  <Stats />
  <Shipment />
  <Feature />
  <Services />
  <CustomRelation />

</div>
</template>
<script setup>
import Header from "@/components/Header.vue";
import Consumer from "@/components/Consumer.vue";
import Stats from "@/components/Stats.vue";
import Shipment from "@/components/Shipment.vue";
import Feature from "@/components/Feature.vue";
import CustomRelation from "@/components/CustomRelation.vue";
import Services from "@/components/Services.vue";
components:{
  Header,Consumer,Stats,Shipment,Feature,CustomRelation,Services
}
</script>