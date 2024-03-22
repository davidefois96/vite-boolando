<script>

import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import products from "./assets/data/db.js"




export default{

components:{

  Header,
  Main,
  Footer,

},


data(){

  return{

    products,


  }

  

  


},

methods:{


},

mounted(){

  console.log(this.products);




}


}

</script>


<template>
  <div>

    <Header />
    <Main />
    <Footer />
    
  </div>
  
</template>

<style lang="scss">

 @use "src/assets/scss/main.scss";

</style>
