<template>
  <div>
  <!-- Begin:: Navbar for PC Laptop -->
    <div class="navbar">
      <div class="navbar-left">
        <div class="navbar-logo-separator">
          <img class="navbar-logo" src="/assets/Logo.png" />
        </div>
        <div class="navbar-menu-links">
          <div class="navbar-link">
            <span class="navbar-link-text" > Quick Facts </span>            
            <img class="navbar-link-dropdown-icon" src="/assets/logical-vee.png" />
          </div>
          <div class="navbar-link">
            <span class="navbar-link-text" > Benefits </span>
            <img class="navbar-link-dropdown-icon" src="/assets/logical-vee.png" />
          </div>
          <span class="navbar-link-text"> Contact </span>
        </div>
      </div>
      <button class="navbar-right"> Get in touch </button>
    </div>
    <!-- End:: Navbar for PC Laptop -->



  </div>
</template>

<script setup>
import { ref } from 'vue'
const showBurgerIcon = ref(false);
</script>

<style scoped lang="scss">
@import "@/assets/scss/main";
.navbar {
  height: 80px;
  background-color: $color-white;
  opacity: 1;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 30px;
  &-left {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &-logo {
    width: $img-max-width-80;
    &-separator{
      border-right: 3px solid lightgray;
    }
  }
  &-menu-links {
    display: flex;
    align-items: center;
    padding: 0 25px;
  }
  &-link {
    display: flex;
    align-items: center;
    margin: 0 10px;
    &-text {
      font-size: 12px;
      font-weight: bold;
      color: $color-secondary;
      &:hover {
        color: $color-primary;
        cursor: pointer;
      }
    }
    &-dropdown-icon {
      margin-left: 8px;
      cursor: pointer;
    }
  }
  &-right{
    width: 151px;
    height: 50px;
    color: $color-white;
    background-color: $color-primary;
    border: unset;
    border-radius: 3px;
    &:hover {
      cursor: pointer;
      background-color: $color-blue-lagoon;
      border: 3px solid #1ECB40;
    }
  }
}



</style>
