<template>
    <div class="shipment">
      <div class="shipment-item left-section">
        <img class="shipment-item-image" src="/assets/dummy.png" />
        <div class="shipment-item-content left-content">
          <span class="shipment-item-content-title"> Lorem ipsum dolor sit amet  </span>
          <hr>
          <p class="shipment-item-content-description">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut
            labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores
            et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr.
          </p>
        </div>
      </div>
      <div class="shipment-item right-section">
        <img class="shipment-item-image" src="/assets/dummy.png" />
        <div class="shipment-item-content right-content">
          <span class="shipment-item-content-title"> Lorem ipsum dolor sit amet  </span>
          <hr>
          <p class="shipment-item-content-description">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut
            labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores
            et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr.
          </p>
          <button class="shipment-item-content-btn">
            More information
          </button>
        </div>
      </div>
      
    </div>
  </template>
  
  <script setup>
 
  </script>
  
  <style scoped lang="scss">
  @import "@/assets/scss/main";
  .shipment {
    &-item {
      display: flex;
      justify-content: center;
      align-items: center;
      &-image {
        width: 50%;
      }
      &-content {
        display: flex;
        flex-direction: column;
        padding-left:6%;
        &-title {
          color: $color-secondary;
          font-weight: $font-weight-bold;
          font-size: $font-size-30;
        }
        &-description {
          font-size: $font-size-16;
          width: 70%;
          color: $color-secondary;
          text-align: left;
        }
        &-btn {
          width: 197px;
          height: 50px;
          color: white;
          background-color: $color-primary;
          border: unset;
          border-radius: 3px;
          margin-top: 20px;
          font-size: $font-size-18;
          font-weight: $font-weight-bold;
          &:hover {
            cursor: pointer;
            background-color: $color-blue-lagoon;
            border: 3px solid $color-green;
          }
        }
      }
    }
  }
  
  .left-content {
    margin-right: 5%;
    hr,
    .shipment-item-content-btn {
      align-self: start;
    }
    .shipment-item-content-description {
      align-self: start;
      width: $element-width-65;
    }
  }
  .right-section {
    flex-direction: row-reverse;
  }
  
  .right-content {
    margin-left: 5%;
  }
  
  hr {
    height: 3px;
    background-color: $color-primary;
    border: none;
    width: 7%;
    margin: 10px 0;
  }
  
  @media only screen and (max-width: 768px) {
    .shipment-item {
      flex-direction: column;
      &-image {
        width: 100%;
      }
      &-content {
        justify-content: center;
        align-items: center;
        margin: 10px auto;
        padding: 20px;
        &-title {
          text-align: center;
        }
        &-description {
          width: 100%;
        }
      }
    }
    .left-content {
      .shipment-item-content-description {
        align-self: center;
        width: 100%;
      }
  
    }
  }
  
  
  </style>
  