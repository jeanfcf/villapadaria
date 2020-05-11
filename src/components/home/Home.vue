<template>
    <div id="home">
        <img class="vetor" src="../../assets/home/vetor_azul_cima.png" alt="desenho" id="vetor1">
        <c-slide/>
        <img class="vetor" src="../../assets/home/vetor_azul_baixo_direita.png" alt="desenho" id="vetor2">
        <img class="vetor" src="../../assets/home/vetor_azul_baixo_esquerda.png" alt="desenho" id="vetor3">

    </div>
</template>

<script>
import cSlide from './Slide';
  export default {
      components:{
          cSlide
      },
      data() {
          return {
              
          }
      },
  }
</script>

<style scoped>

    #home{
        height: 100vh;
        background-color: #1a8acb;
    }

    .vetor{
        position: absolute; 
        overflow: hidden;
    }
    #vetor1{
        right: 0;
        top:0;
    }
    #vetor2{
        right: 0;
        bottom:0;
    }
    #vetor3{
        left: 0;
        bottom:0;
    }
    @media screen and (max-width: 1400px) {
        #vetor1{
            width: 366px;
            height: 285px;
        }
        #vetor2{
            width: 267px;
            height: 290px;
        }
        #vetor3{
            width: 285px;
            height: 225px;
        }
    }
    @media screen and (max-width: 760px) {
        #vetor1{
            width: 302px;
            height: 235px;
        }

    }
    @media screen and (max-width: 600px) {
        #vetor1{
            width: 172px;
            height: 135px;
        }
        #vetor2{
            width: 134.5px;
            height: 130px;
            }
        #vetor3{
            height: 125px;
            width: 159px ;
        }
    }
</style>