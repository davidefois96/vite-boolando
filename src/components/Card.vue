<script>
  export default {

    props:{
      img: String,
      imgSecond: String,


    }
    
  }
</script>

<template>
  <div class="figure">

    <div class="model">

      <img :src="`/assets/img/${img}`" alt="1">
      <img class="hovered" :src="`/assets/img/${imgSecond}`" alt="1b">

      <div class="heart">&#9829</div>
      <div class="discount red">-50%</div>
      <div class="discount sostenibile" id="discount-right">Sostenibilità</div>


    </div>

    <p>
      Levi's <br>
      <strong>RELAXED FIT TEE UNISEX</strong><br>
      <span><strong class="redtext">14,99 &#8364</strong></span>
      <span class="crossed-out">29,99 &#8364</span>
      
    </p>


  </div>  

    
    

  
</template>



<style lang="scss" scoped>

.figure{
 
 width: 32%;
 
 
 cursor: pointer;
}




.figure .model .discount{
 position: absolute;
 top: 88%;
 color: white;
 padding: 7px 12px;
 
}

.discount.red{background-color: red;}

.discount.sostenibile{background-color: green;}


.figure .model .heart {
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