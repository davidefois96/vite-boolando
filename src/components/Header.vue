<script>
  export default {

    data(){

      return{
        type:[

          'Donna',
          'Uomo',
          'Bambini'

        ],
        icons:[
          'fa-regular fa-user',
          'fa-regular fa-heart',
          'fa-solid fa-bag-shopping'

        ]



      }

      
    }
    
  }
</script>

<template>
  <header>
    <div class="container flexing" id="spc-between">

      <ul class="flexing" >
        <li v-for="(element,index) in type"><a class="right" href="#"><strong>{{type[index]}}</strong></a></li>
        
      </ul>

      <img src="/assets/img/boolean-logo.png" alt=""  id="resize-logo">


      <ul class="flexing" >
        <li v-for="(element,index) in icons"><a class="left" href="#"><i :class="`${icons[index]}`"></i></a></li>
        
      </ul>
      
      
      
    </div>

    
  </header>

</template>

<style lang="scss" scoped>

  header{
    background-color: #ff6900;
    display: flex;
    color: #e9e1db;
    align-items: center;
    position: fixed;
    width: 100%;
    padding-top: 25px;
    padding-bottom: 25px;
    z-index: 2;

    .container{
      align-items: center;


    }


}

</style>