<template>
  <div id="burguer">
    <a @click="abrirMenu(); print()">
      <img id="menu" :src="source" alt="menu" width="50" height="50" />
    </a>
    <div id="show">
      <div @click="fecharMenu" class="close"><img src="../../assets/navbar/close.svg" alt="close"></div>
      <ul>
        <a @click="fecharMenu" v-scroll-to="{el: link1, offset: this.height}"><li>
          {{texto1}}
        </li>
        </a>
        <a @click="fecharMenu" v-scroll-to="{el: link2, offset: this.height}"><li>
          {{texto2}}
        </li>
        </a>
        <a @click="fecharMenu" v-scroll-to="link3"><li>
          {{texto3}}
        </li>
        </a>
        <a @click="fecharMenu" v-scroll-to="link4"><li>
          {{texto4}}
        </li>
        </a>
        <a @click="fecharMenu" v-scroll-to="{el: link5, offset: this.height}"><li>
          {{texto5}}
        </li>
        </a>
        <a @click="fecharMenu" v-scroll-to="{el: link5, offset: this.height}"><li>
          {{texto5}}
        </li>
        </a>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      height: 0,
    }
  },
  props: {
    link1: String,
    link2: String,
    link3: String,
    link4: String,
    link5: String,
    link6: String,
    texto1: String,
    texto2: String,
    texto3: String,
    texto4: String,
    texto5: String,
    texto6: String,
    source: String
  },
  methods: {
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
    abrirMenu() {
      document.getElementById("menu").style.display = "none";
      document.getElementById("show").style.transform = 'translateX(100vw)'
    },
    fecharMenu() {
      document.getElementById("menu").style.display = "block";
      document.getElementById("show").style.transform = 'translateX(-100vw)'
    },
  }
};
</script>

<style scoped>
#menu{
  cursor: pointer;
  margin-right: 10px;
}
.close {
  position: absolute;
  margin-top: 20px;
  margin-right: 20px;
  top: 0;
  right: 0;
  cursor: pointer;
  width: 30px ;
  height: 30px;
}
#show {
display: flex;
  margin-left: 5%;
  justify-content: center;
  
  align-items: center;
  width: 100%;
  height: 100vh;
  position: absolute;
  
  top: 0;
  right: 100vw;
  z-index: 10;
  background-color: white;
transition: all .2s linear ;
}

#show ul {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  padding-top: 5%;
  padding-bottom: 5%;
}
#show ul li{
    padding: 5%;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40VW;
    height: 10vh;
    background-color: #1a8acb;
    list-style: none;
    cursor: pointer;
    text-align: center;
}
#show ul li:hover{
    opacity: 0.8;
}

#show ul li a{
    text-decoration: none;
    font-size: 20px;
    font-weight: bold;
    color: #000;
}
@media screen and (max-width: 375px) {
  #menu{
    width: 30px;
    height: 30px;
    margin-right: 20px;
  }
  .close{
    width: 20px !important;
    height: 20px !important;
  }
}
</style>