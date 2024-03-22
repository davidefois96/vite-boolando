<script>

import {products} from "../assets/data/products.js" ;
import Card from "../components/Card.vue";

  export default {

    components:{

      Card,
      
    },

    
    data(){
      return{

        products


      }

  
    },

    mounted(){


      console.log(products);
    }

    
  }

</script>

<template>

<main class="container flexing">

  <Card v-for="(product) in products"
  :img="product.frontImage"
  :imgSecond="product.backImage"
  :brand="product.brand"
  :price="product.price"
  :name="product.name"
  :badges="product.badges"
  :cardId="product.id"
  :isInFavorites="product.isInFavorites"

  />

</main>

  
</template>


<style lang="scss" scoped>

main{
  padding-top: 150px;
  padding-bottom: 30px;
  
}


main.container{
  
  background-position: center;
  justify-content: center;
  gap: 1%;
  flex-wrap: wrap;
 
}

</style>