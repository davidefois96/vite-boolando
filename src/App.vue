<script>

import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";





export default{

components:{

  Header,
  Main,
  Footer,

},


data(){

  return{

    


  }

  

  


},

methods:{


},

mounted(){

  

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
