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

  <Card v-for="(product,index) in products"
  :img="product.frontImage"
  :imgSecond="product.backImage"
  
  
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