<script>
  import Products from "./assets/data/db.js";

  export default {

    props:{

      img: String,
      secImg: String,
      id: Number,
      brand: String,
      name: String,
      price: Number,
      type: String,
      value:String

    },
    data(){


      return{

        Products,

      }



    },

    methods:{


    },

    mounted(){




  }

    
}
</script>

<template>

<div class="card">



  <div class="model">

    <img :src="img" alt="1">
    <img class="hovered" :src="secImg" alt="1b">

    <div class="heart">&#9829</div>
    <div :class="type">{{value}}</div>
    <div :class="type" id="discount-right">{{value}}</div>


  </div>

  <p>
    <p>{{ brand }}</p> <br>
    <strong>{{ name }}</strong><br>
    <span><strong class="redtext">14.99 &#8364</strong></span>
    <span class="crossed-out">{{ price }} &#8364</span>
    
  </p>



</div>

  

  
</template>



<style lang="scss" scoped>

.card{
 
 width: 32%;
 
 cursor: pointer;
}




.card .model .discount{
 position: absolute;
 top: 88%;
 color: white;
 padding: 7px 12px;
 
}

.tag{background-color: red;}

.discount{background-color: green;}


.card .model .heart {
 position: absolute;
 padding: 10px 20px;
 background-color: white;
 right: 0;
 top: 3%;
 font-size: 2rem;

}

.heart:hover {color: red;} 

.model{position: relative;}

.model:hover .hovered{
 display: block;
}


span > strong.redtext{color: red;}

span.crossed-out{
 text-decoration: line-through;
 margin-left: 3px;
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