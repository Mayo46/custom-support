<template>
  <div>
  <!-- Begin:: Navbar for PC Laptop -->
    <div class="navbar">
      <div class="navbar-left">
        <div class="navbar-logo-separator">
          <img class="navbar-logo" src="/assets/logo.png" />
        </div>
        <div class="navbar-menu-links">
          <div class="navbar-link">
            <span class="navbar-link-text" > {{ optionOneTitle }} </span>            
            <img class="navbar-link-dropdown-icon" src="/assets/logical-vee.png" />
          </div>
          <div class="navbar-link">
            <span class="navbar-link-text" > {{ optionTwoTitle }} </span>
            <img class="navbar-link-dropdown-icon" src="/assets/logical-vee.png" />
          </div>
          <span class="navbar-link-text"> {{ contactTitle }} </span>
        </div>
      </div>
      <button class="navbar-right"> {{ btnText }} </button>
    </div>
    <!-- End:: Navbar for PC Laptop -->
    <!-- Begin::Navbar Controls -->
    <div class="mobile-navbar-controls">
      <div class="navbar-logo-outer">
        <img class="navbar-logo" src="/assets/logo.png" />
      </div>
      <!-- &#9776 this is the unicode of Burger Icon
       picking form https://www.w3schools.com/charsets/ref_utf_symbols.asp -->
      <span class="mobile-navbar-controls-icon" v-if="!showBurgerIcon" @click="showBurgerIcon = true" > &#9776; </span>
      <span class="mobile-navbar-controls-icon" v-else @click="showBurgerIcon = false" >
        <img src="/assets/cross.png" />
      </span>
    </div>
    <!-- End:: Navbar Controls -->
    <!-- Begin:: Navbar for Mobile -->
    <div class="mobile-navbar" v-if="showBurgerIcon">
      <div class="mobile-navbar-links">
        <span class="mobile-navbar-link"> {{ optionOneTitle }} </span>
        <span class="mobile-navbar-separator"></span>
        <span class="mobile-navbar-link"> {{ optionTwoTitle }} </span>
        <span class="mobile-navbar-separator"></span>
        <span class="mobile-navbar-link"> {{ contactTitle }} </span>
      </div>
    </div>
    <!-- End:: Navbar for Mobile -->


  </div>
</template>

<script setup>
import { ref } from 'vue'
const showBurgerIcon = ref(false);
const btnText = 'Get in touch';
const contactTitle = 'Contact';
const optionOneTitle = 'Quick Facts';
const optionTwoTitle = 'Benefits';
</script>

<style scoped lang="scss">
@import "@/assets/scss/main";
</style>
