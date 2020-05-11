<template>
  <div id="onde">
    <div class="onde-mapa">
      <iframe
        id="mapa-frame"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d554.9162844411004!2d-40.50677842332488!3d-7.575665544701536!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x79fa9fa3e11ab23%3A0xa17eb45ad9a4bf07!2sVILLA%20GOURMET!5e0!3m2!1sen!2sbr!4v1589225770954!5m2!1sen!2sbr"
        width="600"
        height="450"
        frameborder="0"
        style="border-radius: 50px;"
        allowfullscreen
        aria-hidden="false"
        tabindex="0"
      ></iframe>
    </div>
    <div class="onde-texto">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam, ipsam. Quam accusantium, optio minus adipisci fugiat, explicabo nulla, exercitationem expedita quas in ipsum doloribus aliquam itaque? Quaerat consequuntur dolores at?</p>
      <div class="onde-foto" />
    </div>
    <div class="vetores">
      <img class="vetor" id="onde-vetor1" src="../assets/onde/canto_cima_esquerdo.svg" alt="vetor" />
      <img class="vetor" id="onde-vetor2" src="../assets/onde/canto_cima_direito.svg" alt="vetor" />
      <img class="vetor" id="onde-vetor3" src="../assets/onde/canto_baixo_esquerdo.svg" alt="vetor" />
      <img class="vetor" id="onde-vetor4" src="../assets/onde/canto_baixo_direito.svg" alt="vetor" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style scoped>
.vetores {
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
  opacity: 0.6;
}
#onde {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  min-height: 100vh;
  padding-top: 5%;
  padding-bottom: 5%;
  background-color: #dcdfde;
}

.onde-mapa {
  z-index: 10;
}
.onde-texto {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 45%;
  z-index: 10;
}
.onde-texto p {
  margin-bottom: 4%;
}
.onde-foto {
  width: 80%;
  height: 250px;
  background-color: #c4c4c4;
  z-index: 10;
}

.vetor {
  position: absolute;
  overflow: hidden;
}
#onde-vetor1 {
  left: 0;
  top: 0;
}
#onde-vetor2 {
  right: 0;
  top: 0;
}
#onde-vetor3 {
  left: 0;
  bottom: 0;
}
#onde-vetor4 {
  right: 0;
  bottom: 0;
}
@media screen and (max-height: 666px){
    .vetores{
        display: none;
    }
}
@media screen and (max-width: 1160px) {
  #mapa-frame {
    width: 440px;
    height: 330px;
  }
}
@media screen and (max-width: 975px) {
  #onde {
    flex-direction: column-reverse;
    justify-content: center;
  }
  #mapa-frame {
    width: 700px;
    height: 400px;
  }
  .onde-texto {
    width: 70%;
    margin-bottom: 5%;
  }
  .onde-texto p {
    font-size: 20px;
  }
  .onde-foto {
    width: 100%;
    height: 30vh;
  }
}

@media screen and (max-width: 800px) {
  #onde-vetor1 {
    width: 189.5px;
    height: 163px;
  }
  #onde-vetor2 {
    width: 275.5px;
    height: 187px;
  }
  #onde-vetor3 {
    width: 116.5px;
    height: 50px;
  }
  #onde-vetor4 {
    width: 314px;
    height: 333px;
  }
}
@media screen and (max-width: 770px) {
  #mapa-frame {
    width: 500px;
    height: 400px;
  }
  
}

@media screen and (max-width: 550px) {
  .onde-texto p {
    font-size: 16px;
  }
  #mapa-frame {
    width: 300px;
    height: 300px;
  }
  #onde-vetor2 {
    width: 202px;
    height: 137px;
  }
  #onde-vetor4 {
    width: 257px;
    height: 283px;
  }
}
@media screen and (max-width: 420px) {
  #onde-vetor2 {
    width: 128.5px;
    height: 87px;
  }
  #onde-vetor4 {
    width: 210px;
    height: 233px;
  }
}
</style>