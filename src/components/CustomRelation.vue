<template>
<div class="testimonial">
 <div class="testimonial-background">    
    <div class="testimonial-section">
        <span class="testimonial-title">
            {{ title }}
        </span>
        <hr>
        <p class="testimonial-description">
            {{ description }}
        </p>
        <button class="testimonial-button desktop-view">
            {{ btnText }}
        </button>
    </div>
 </div>  
</div>
</template>
  
<script setup>
  const title = 'Customs clearance after Brexit';
  const description = 'Since 4 years we are successfully helping our customers to prepare their business for Brexit. Our Bexit customs agents are always up-to-date with the latest customs regulations after Brexit and look forward to support you with Brexit customs procedures.';
  const btnText = 'Brexit and Custom: get ready!';
</script>
<style scoped lang="scss">
@import "@/assets/scss/main";
.testimonial{
  background: url("/assets/relationship.png");
  height:600px;
 &-background{
    background: transparent url("assets/background-green.png") 0% 0% no-repeat padding-box;
    opacity: 0.3;
    width: 50%;
    height: 600px;
 } 
 &-section{
    width: 65%;
    display: flex;
    flex-direction: column;
    margin-left: 21%;
 }
 &-title {
    margin-top:10rem;
    font-size: $font-size-30;
    color: $color-white;
    text-align: left;
    font-weight: $font-weight-bold;
}
&-description {
    color: $color-white;
    font-size: $font-size-16;
}
&-button {
    width: 289px;
    height: $element-height-50;
    color: $color-white;
    background-color: $color-primary;
    border: unset;
    border-radius: 3px;
    margin-top: 20px;
    font-size: $font-size-16;
    font-weight: $font-weight-bold;
    &:hover {
      cursor: pointer;
      color: $color-primary;
      background-color: $color-white;
      border: 3px solid $color-green;
    }
}

}
@media only screen and (max-width: 768px) {

  
  .testimonial{
    &-background{
      width: 100%;
    }
    &-section{
        margin-left:10%;
        width:auto;
    }
    &-title{
        font-size: $font-size-25;
    }
  }
  
}
</style>
  