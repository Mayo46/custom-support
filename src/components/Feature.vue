<template>
 <div class="feature">
     <span class="feature-title">{{ featureTitle }}</span>
     <button class="feature-button">{{ btnText }}</button>
 </div>
 <hr>
 <div class="feature-categories">
     <div v-for="(item,index) in featureItems" :key="index" class="feature-categories-item">
         <img :src="item.icon" />
         <br />
         <span class="feature-categories-item-title">{{ item.title }}</span>
         <p class="feature-categories-item-description">{{ item.description }}</p>
     </div>
 </div>


 <!-- Begin:: Shipping Image Section -->
 <div>
    <img class="shipping-logo" src="/assets/Shiping-logo.png" />   
 </div>   
  <!-- End:: Shipping Image Section -->
</template>
<script setup>
const featureTitle="We offer end-to-end customs services with fast, accurate and compliant customs in multiple countries";
const btnText="Get in touch";
const featureItems = [
   {
       title: 'Fast and accurate',
       icon: '/assets/accurate.png',
       description:"We offer you a full service offering with fast and accurate customs in multiple countries."
   }, 
   {
       title: 'Strict Compliance',
       icon: '/assets/compliance.png',
       description:"We make sure you are compilant with religious to migrate custom-related risk and exposure."
   },
   {
       title: 'Qualified Professionals',
       icon: '/assets/professional.png',
       description:"Over highly skilled professionals offer custom export advice to optmize your duty managment and help you save costs."
   },
   {
       title: 'Online and real-time control',
       icon: '/assets/time-control.png',
       description:"Real time finacne dashboard to manage your custom clearance protfolio."
   }, 
   {
       title: 'EU-wide coverage',
       icon: '/assets/coverage.png',
       description:"We have offices in 5 Europen countries but thanks to our network of trusted partners we have EU-wide coverage."
   },
   {
       title: 'Innovation & digitalisation',
       icon: '/assets/innovation.png',
       description:"We used advanced IT-tools for customer declaration and customs clearance."
   }
  ];

</script>
<style scoped lang="scss">
@import "@/assets/scss/main";
.feature{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding-top: 40px;
    &-title{
     color: $color-secondary;
     font-weight: $font-weight-bold;
     font-size: $font-size-25;
     width: 889px;
    
    }
    &-button {
      width: 151px;
      height: $element-height-50;
      color: $color-white;
      background-color: $color-primary;
      border: unset;
      border-radius: 3px;
      &:hover {
        cursor: pointer;
        background-color: $color-blue-lagoon;
        border: 3px solid $color-green;
      }
    }
    
}
.feature-categories{
    max-width: 1140px;
    margin:0 auto;
    display: grid;
    grid-template-columns: auto auto auto;
    &-item{
        padding: 10px;
    }
    &-item-title{
        color: $color-secondary;
        font-weight: $font-weight-bold;
        font-size: $font-size-14;
        &:hover {
            cursor: pointer;
            color: $color-primary;
 
      }
    }
}
hr {
    height: 3px;
    background-color: #01A4B7;
    border: none;
    width: 3%;
    margin: 2% 10.5%;
  }
.shipping-logo{
    height:550px
}
@media only screen and (max-width: 768px) {
    .shipping-logo {
      width:333px;
      height:300px;
    }
    .feature-categories{
        display: flex;
        flex-direction: column;
        &-item{
            width:auto;
        }
        &-item-description{
            width:75%;
        }
    }
    .feature{
      flex-direction: column;
      justify-content: center;
      &-title{
        width: 300px;
        }
      &-button {
       width:300px;  
      }  
    }
   
    
  }
</style>