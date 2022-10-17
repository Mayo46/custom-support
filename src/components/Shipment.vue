<template>
    <div class="gallery">
      <div class="gallery__item left">
        <img class="gallery__item__graphic" src="/assets/dummy.png" />
        <div class="gallery__item__content left-content">
          <span class="gallery__item__content__heading"> Lorem ipsum dolor sit amet  </span>
          <hr>
          <p class="gallery__item__content__detail">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut
            labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores
            et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr.
          </p>
        </div>
      </div>
      <div class="gallery__item right">
        <img class="gallery__item__graphic" src="/assets/dummy.png" />
        <div class="gallery__item__content right-content">
          <span class="gallery__item__content__heading"> Lorem ipsum dolor sit amet  </span>
          <hr>
          <p class="gallery__item__content__detail">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut
            labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores
            et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr.
          </p>
          <button class="gallery__item__content__btn">
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
  .gallery {
    &__item {
      display: flex;
      justify-content: center;
      align-items: center;
      &__graphic {
        width: 50%;
      }
      &__content {
        display: flex;
        flex-direction: column;
        &__heading {
          color: #3D4D62;
          font-weight: bold;
          font-size: 30px;
        }
        &__detail {
          font-size: 16px;
          width: 70%;
          color: #3D4D62;
          text-align: left;
        }
        &__btn {
          width: 197px;
          height: 50px;
          color: white;
          background-color: #01A4B7;
          border: unset;
          border-radius: 3px;
          margin-top: 20px;
          font-size: 18px;
          font-weight: bold;
          &:hover {
            cursor: pointer;
            background-color: $color-blue-lagoon;
            border: 3px solid $color-green;
          }
        }
      }
    }
  }
  
  
  .right {
    flex-direction: row-reverse;
  }
  
  .left-content {
    margin-right: 5%;
    text-align: right;
    hr,
    .gallery__item__content__btn {
      align-self: center;
    }
    .gallery__item__content__detail {
      align-self: end;
      width: 65%;
    }
  }
  
  .right-content {
    margin-left: 5%;
  }
  
  hr {
    height: 3px;
    background-color: #01A4B7;
    border: none;
    width: 7%;
    margin: 10px 0;
  }
  
  @media only screen and (max-width: 768px) {
    .gallery__item {
      flex-direction: column;
      &__graphic {
        width: 100%;
      }
      &__content {
        justify-content: center;
        align-items: center;
        margin: 10px auto;
        padding: 20px;
        &__heading {
          text-align: center;
        }
        &__detail {
          width: 100%;
        }
      }
    }
    .left-content {
      .gallery__item__content__detail {
        align-self: center;
        width: 100%;
      }
  
    }
  }
  
  
  </style>
  