<script>

  import card from "./Card.vue";
  
  import Products from "./assets/data/db.js";


  export default {

    components:{

      card,
      

    },
    data(){

  

      return{

        Products,

      }



    },

    
  }

</script>

<template>

<main class="container flexing">

<card 
 v-for="(product,index) in products"

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