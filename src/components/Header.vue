<template>
    <div class="header">
      <div class="header-section">
        <span class="header-title">
          {{ headerTitle }}
        </span>
        <hr>
        <p class="header-description">
          {{ headerDescription }}
        </p>
        <button class="header-button desktop-view">
          {{ btnText }}
        </button>
      </div>
      <div class="header-features">
        <p v-for="(item,index) in headerItems" :key="index">
            <img :src="item.icon" />
            <span class="header-features-text"> {{ item.text }}</span>
        </p>
      </div>
      <button class="header-button mobile-view">
        {{ btnText }}
      </button>
  
    </div>
  </template>
  
<script setup>
  const headerTitle = 'Headache on complex customs matters for your business?';
  const headerDescription = 'Customs Support is your neutral full-service customs broker for complex customs matters with 20+ years of expertise in Europe and over 400 customs specialists who are happy to take the load off your mind!';
  const btnText = 'Get your quote now';
  const headerItems = [
   {
       text: 'Fast and accurate customs clearance delivery',
       icon: '/assets/tick.png'
   }, 
   {
       text: 'EU-wide customs coverage',
       icon: '/assets/tick.png'
   },
  {
       text: 'Online and real-time control of customs processes',
       icon: '/assets/tick.png'
   }
  ];
</script>

  