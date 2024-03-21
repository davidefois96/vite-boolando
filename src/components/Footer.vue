<script>
  export default {
    data(){

      return{
        faq:[

          'Informazioni legali',
          'Informazioni sulla privacy',
          'Diritto di recesso'

        ],
        icons:[
          'fa-brands fa-twitter',
          'fa-brands fa-facebook',
          'fa-brands fa-instagram',
          'fa-brands fa-pinterest',
          'fa-brands fa-youtube'

        ]



      }


    }
    
  }
</script>

<template>
  <footer>

    <div class="container flexing" id="spc-between">

      <div>

        <p>

          <strong>Boolando s.r.l.</strong> <br>
          
        </p>

        <ul>

          <li class="flexing">

            <a v-for="(element,index) in faq" class="right" href="#">{{faq[index]}}</a>
            
          </li>

        </ul>

      </div>

      <div>

        <p>

          <strong>Trovaci anche su</strong> <br>
          
        </p>

        <ul>
          <li class="flexing">

            <a v-for="(element,index) in icons" class="left" href="#"><i :class="`${icons[index]}`"></i></a>
            
          </li>
        </ul>

      </div>

      



    </div>


  </footer>
</template>


<style lang="scss" scoped>

footer{
  padding-top: 30px;
  padding-bottom: 30px;
  background-color: #1a1a1a;
  color: #e9e1db;
  line-height: 25px;
  border-bottom: solid #f6f6f6 2px;

}


</style>