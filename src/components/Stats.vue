<template>
  <div class="stats">
    <span class="stats-title">{{ statsTitle }}</span>
    <hr>
    <div class="stats-detail">
      <div class="stats-detail-setion" v-for="(item, index) in statsData" :key="index">
        <span class="stats-detail-number"> {{item.number}} </span>
        <span  class="stats-detail-text"> {{item.text}} </span>
      </div>
    </div>
    <button class="stats-button">
      {{ btnText }}
    </button>
  </div>
</template>
<script setup>
const statsTitle='The leading customs agent in Europe and UK';
const btnText='Get in touch';
const statsData = [
        {
          number : '20 +',
          text : 'years of experience'
        },
        {
          number : '400',
          text : 'qualified customs specialists'
        },
        {
          number : '200',
          text : 'strategic locations'
        },
        {
          number : '5',
          text : 'countries'
        }
      ]
</script>
<style scoped lang="scss">
  @import "@/assets/scss/main";
  .stats {
  background-color: #006B6E;
  min-height: 438px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  &-title {
    font-size: 40px;
    font-weight: bold;
    color: white;
  }
  &-detail {
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    &-setion {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      margin: 20px 20px;
      border-right: 3px solid lightgray;
      padding: 10px;
      &:last-child {
        border: none;
      }
    }
    &-number {
      font-size: 50px;
      font-weight: bold;
    }
    &-text {
      font-size: 20px;
      font-weight: bold;
      text-align: center;
    }
  }
  &-button {
    width: 151px;
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
      color: #01A4B7;
      background-color: white;
      border: 3px solid $color-green;
    }
  }
}

hr {
  height: 3px;
  background-color: #01A4B7;
  border: none;
  width: 5%;
  margin: 10px auto;
}

@media only screen and (max-width: 768px) {
  .stats {
    padding: 30px;
    &-title {
      text-align: center;
    }
    &-detail {
      flex-direction: column;
      &-setion {
        border-right: unset;
        border-bottom : 1px solid lightgray;
        width: 100%;
      }
    }
  }
}
</style>