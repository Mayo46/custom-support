<template>
  <div class="footer">
    <div class="footer-items">
      <span class="footer-item" v-for="(item,index) in footerItems" :key="index"> {{ item }} </span>
    </div>
    <div class="footer-text">
      <span> {{ copyRightText }} </span>
    </div>
  </div>
</template>

<script setup>
  const copyRightText = '© 2021 Customs Support Group. All rights reserved.';
  const footerItems = ['Imprint', 'Data Security', 'Conditions', 'Cookies', 'Custom Support'];
</script>

