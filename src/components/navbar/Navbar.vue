<template>
  <div v-on:mouseover="print" id="navbar">
    <a href="#"><img v-scroll="handleScroll" id="logo" src="../../assets/navbar/logo_branca.svg" alt="logo" ></a>
    <c-burguer 
    class="show"
    :source="burguer" 
    link1="#inicio" 
    link2="#home" 
    link3="#home" 
    link4="#home" 
    link5="#home" 
    link6="#home" 
    texto1="HOME" 
    texto2="SOBRE" 
    texto3="DELIVERY" 
    texto4="PORTFÓLIO" 
    texto5="ONDE ESTAMOS?" 
    texto6="CONTATO" 
    />
    <ul>
      <li>
        <a  :class="{black: aplicar}" v-scroll-to="{el: '#inicio',offset: this.height}">INÍCIO</a>
      </li>
      <li>
        <a :class="{black: aplicar}" v-scroll-to="{el: '#home',offset: this.height}">SOBRE</a>
      </li>
      <li>
        <a :class="{black: aplicar}" v-scroll-to="'#home'">DELIVERY</a>
      </li>
      <li>
        <a :class="{black: aplicar}" v-scroll-to="'#home'">PORTFÓLIO</a>
      </li>
      <li>
        <a :class="{black: aplicar}" v-scroll-to="'#home'">ONDE ESTAMOS?</a>
      </li>
      <li>
        <a :class="{black: aplicar}" v-scroll-to="'#home'">CONTATO</a>
      </li>
    </ul>
  </div>
</template>

<script>
import cBurguer from './Burguer'
export default {
  components:{
    cBurguer
  },
 data() {
   return {
     height: 0,
     aplicar: false,
     burguer: require('@/assets/navbar/menu_branca.svg')
   }
 },
   methods:{
     print(){
       let alt = window.innerWidth;
       if(alt < 375){
         this.height = -60;
       }else if(alt < 760){
         this.height = -85;
       }else if(alt < 1350){
         this.height = -110;
       }else{
         this.height = -135;
       }
       },
    handleScroll: function (evt, el) {
      if (window.scrollY > 0) {
        el.setAttribute(
          'src',
          require('@/assets/navbar/logo_azul.svg')
        )
        document.getElementById('navbar').style.backgroundColor = 'white';
        if(window.innerWidth > 360){
        document.getElementById('logo').style.marginTop = 0;
        }
        this.aplicar = true;
        this.burguer = require('@/assets/navbar/menu_azul.svg')
      }else{
        el.setAttribute(
          'src',
          require('@/assets/navbar/logo_branca.svg')
        )
        document.getElementById('navbar').style.backgroundColor = 'transparent';
        document.getElementById('logo').style.marginTop = '15%';
        this.aplicar =false;
        this.burguer = require('@/assets/navbar/menu_branca.svg')
      }
    }
  }
};
</script>

<style scoped>
.show{
  display: none;
}
#navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    position: fixed;
    padding-left: 5%;
    padding-right: 3%;
    transition: all 0.2s ease-in 0.1s;
    z-index: 100;
}

#logo{
    margin-top: 15%;
    height: 131px;
    width: 302.25px;
    transition: all  0.3s ease-in-out 0.1s;
}
#navbar ul{
    display: flex;
    justify-content: space-around;
    width: 100%;
}
#navbar ul li{
    display: inline;
}
#navbar ul li a{
    text-decoration: none;
    color: white;
}
#navbar ul li a:hover{
    color: #5f6364;
}

.black{
  color: #5f6364 !important;
}
.black:hover{
  color: #1a8acb !important;
}
@media screen and (max-width: 1350px) {
#logo{
  width: 250.25px;
  height: 106px ;
}
#navbar ul li a{
  font-size: 14px;
  cursor: pointer;
}
}
@media screen and (max-width: 972px) {

.show{display: block}
#navbar{
  padding-left: 10%;
}
#navbar ul{
  display: none;
}
  
#logo{
  width: 249.7px;
  height: 106px ;
}

#menu{ display: block;
  margin-right: 50px;
  width: 50px;
  height: 50px;
}
}

@media screen and (max-width: 760px) {
#logo{
  width: 197.2px;
  height: 81px ;
}
#menu{
  width: 35px;
  height: 35px;
}
}
@media screen and (max-width: 374px) {
#logo{
  width: 144.7px;
  height: 56px ;
}
#menu{
  width: 25px;
  height: 25px;
  margin-right: 25px;
}
}
</style>