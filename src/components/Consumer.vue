<template>
    <div class="consumers">
        <!-- <div class="consumers-card"></div> -->
      <!-- <div style="background: url('/assets/grey.png')" class="test"> </div>  -->
      <img class="consumers-image" src="/assets/consumer.png" />
      
      <div class="consumers-content">
        <span class="consumers-content-title">
            {{ consumerTitle }}
        </span>
        <hr>
        <p class="consumers-content-description">
          We are the trusted partner for customs matters of more than 7000 companies across Europe.
          Since 20 years we successfully operate with customers from small and large good owners
          to freight forwarders and digital platforms across various industries.
        </p>
      </div>
    </div>
  </template>
  
  <script setup>
  const consumerTitle = ' Who we work with';

  </script>
  
  <style scoped lang="scss">
  @import "@/assets/scss/main";
  .consumers {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 20px;
    &-card {
      background: url('/assets/grey.png');
      width: 100%;
      height: 100%;
      position: absolute;
      z-index: -1;
    }
    &-image {
     
      background-color: #F0F0F0;
    }
    &-content {
      width:26%;
      &-title {
        color: $color-secondary;
        font-size: $font-size-30;
        font-weight: $font-weight-bold;
      }
      &-description {
        color: $color-black-shadow;
        font-size: $font-size-16;
      }
    }
  }
  
  hr {
    height: 3px;
    background-color:$color-primary;
    border: none;
    width: 10%;
    margin: 10px 0;
  }
  
  @media only screen and (max-width: 768px) {
    .consumers {
      flex-direction:  column;
      &-image {
        height: auto;
        margin-bottom: 20px;
        width: 90%;
      }
      &-content {
        width: 90%;
      }
    }
  }
  
  </style>
  