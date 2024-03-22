<script>
  import {products} from "../assets/data/products.js" ;
  export default {

    props:{
      img: String,
      imgSecond: String,
      brand:String,
      price: Number,
      name: String,
      badges: Array,
      cardId: Number


    },
    data(){

      return{
        products



      }



    }
    
  }
</script>

<template>
  <div class="figure">

    <div class="model">

      <img :src="`/assets/img/${img}`" alt="">
      <img class="hovered" :src="`/assets/img/${imgSecond}`" :alt="cardId">



      <div class="heart">&#9829</div>

      <div class="badgesContainer">

        <span v-for="(badge,index) in badges" :class="badge.type">

          {{ badge.value }}

        </span>
        

      </div>

      
    </div>

    

    <p>
      {{ brand }} <br>
      <strong>{{ name }}</strong><br>
      <span><strong class="redtext">{{price}}&#8364</strong></span>
      <span class="crossed-out">29.99 &#8364</span>
      
    </p>


  </div>  

    
    

  
</template>



<style lang="scss" scoped>

.figure{
 
 width: 32%;
 cursor: pointer;

 .model{

  position: relative;

  &:hover{

    .hovered{
      display: block;
    }


  }

  .heart{
    position: absolute;
    padding: 10px 20px;
    background-color: white;
    right: 0;
    top: 3%;
    font-size: 2rem;

    &:hover{
      color: red;


    }


  }

 }
}

span{
  strong.redtext{
    color: red;
    margin-right: 5px;
  }

  .crossed-out{
    text-decoration: line-through;
   
  }
 
}


.badgesContainer{
 position: absolute;
 top: 88%;
 
}

.discount{
  background-color: red;
  color: white;
  padding: 7px 12px;
 
}

.tag{
  background-color: green;
  color: white;
  padding: 7px 12px;
 
}

div.figure p {
 margin-bottom: 40px;
}

.hovered{
 display: none;
 position: absolute;
 top: 0;
 left: 0;

}

</style>