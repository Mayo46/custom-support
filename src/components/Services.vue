<template>
 <div class="title">{{ title }}</div>  
 <hr> 
 <div class="services">
    <div v-for="(item,index) in serviceItems" :key="index" class="services-item">
        <div class="bg-img-height photo" :style="`background-image: url('/assets/service.png')`">

            <!-- <img class="photo" :src="item.icon" /> -->
            <div class="overlay"> 
                <p> {{ btnText }} ></p>
            </div>
         </div>

         <br />
         <span class="services-item-title">{{ item.title }}</span>
         <p class="services-item-description">{{ item.description }}</p>
         <span class="services-item-button">{{ btnText }} <span class="services-item-icon"> &#8250 </span></span>
     </div>
 </div>
</template>
<script setup>
const title="Customs Support is a full-service provider for customs services and is here to help";
const btnText="Learn More";
const serviceItems = [
   {
       title: 'Import customs clearance',
       icon: '/assets/service.png',
       description:"If you would like to import goods from a third country to within the European Union, Customs Support assists you in every step of the customs clearance process. Our customs experts take care of import documents, classification of import goods with the correct HS code, coordination of physical inspection and duty management.",
       btnText:"Learn more"
    }, 
   {
       title: 'Export customs clearance',
       icon: '/assets/service.png',
       description:"If you would like to export goods from a third country to within the European Union, Customs Support assists you in every step of the customs clearance process. Our customs experts take care of export documents, classification of export goods with the correct HS code, coordination of physical inspection and duty management.",
       btnText:"Learn more"
    },
   {
       title: 'Customs transit procedures',
       icon: '/assets/service.png',
       description:"We assist you in all requirements for different types of transit procedures and ensure the correct handling of customs clearance. Our customs experts take care of T1 transit declarations and arrange the transport of the goods, accompanied by the correct transit documents.",
       btnText:"Learn more"
    },

  ];
</script>
<style scoped lang="scss">
@import "@/assets/scss/main";
.title {
    font-size: $font-size-25;
    text-align: center;
    font-weight: $font-weight-bold;
    color: $color-secondary;
    width: 889px;
    margin: 0 auto;
}

hr {
    height: 3px;
    background-color: $color-primary;
    border: none;
    width: 3%;
    margin: 15px auto;
}

.services {
    max-width: 1140px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: auto auto auto;
    margin-bottom: 40px;

    &-item {
        padding: 10px;
        width: 85%;
    }

    &-item-title {
        color: $color-secondary;
        font-size: $font-size-20;
        font-weight: $font-weight-bold;
    }

    &-item-description {
        color: $color-secondary;
        font-size: $font-size-16;
        // font-family: $font-family-regular;
        font-weight: $font-weight-normal;
    }

    &-item-button {
        color: $color-primary;
        font-size: $font-size-16;
        font-weight: $font-weight-bold;
        cursor: pointer;
    }

    &-item-icon {
        font-size: $font-size-20;
        font-weight: $font-weight-bold;
    }
}

.bg-img-height {
    height: 226px;
    background-position: 50%;
    background-repeat: no-repeat;
    background-size: contain;
    cursor: pointer;
    vertical-align: top;
    position: relative;
}

.photo .overlay {
    background: $color-primary;
    bottom: 0;
    color: white;
    font-size: 1em;
    left: 0;
    opacity: 0;
    overflow: hidden;
    padding: 1.75em 3em;
    position: absolute;
    text-align: center;
    top: 0;
    right: 0;
    transition: 0.6s;
    border: 3px solid $color-green;
}

.photo .overlay:hover {
    opacity: 1;
}

.photo .overlay p {
    font-size: $font-size-18;
    margin-top: 70px;
}

@media only screen and (max-width: 768px) {
    .title {
        width: 310px
    }

    .services {
        display: block;

        &-item-title {
            padding-left:12px;
        }

        &-item-description {
            padding: 0 12px;
            text-align: left;
        }

        &-item-button {
            padding: 0 12px;
            text-align: left;
        }
    }


}
 
</style>