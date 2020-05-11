<template>
  <div id="sobre">
      <c-slide/>
     <div id="sobre2">
    <div id="gourmet" class="villa">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
      <img class="villa-logo" src="../../assets/sobre/villa_gourmet.svg" alt="gourmet" />
      <div class="villa-img"></div>
    </div>
    <div id="padaria" class="villa">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
      <img class="villa-logo" src="../../assets/sobre/villa_padaria.svg" alt="padaria" />
      <div class="villa-img"></div>
    </div>
    <div id="bistro" class="villa">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
      <img class="villa-logo" src="../../assets/sobre/villa_bistro.svg" alt="bistro" />
      <div class="villa-img"></div>
    </div>
    </div> 
  </div>
</template>

<script>
import cSlide from './SlideSobre';
  export default {
      components:{
          cSlide
      },
      data() {
          return {
              
          }
      },
  };
</script>

<style scoped>
#sobre{
    width: 100%;
    min-height: 100vh;
}
#slidesobre{
    display: none;
}
#sobre2 {
  display: inline-grid;
  grid-template-columns: 1fr 1fr 1fr;
  width: 100%;
  min-height: 100vh;
}
#sobre2 p {
    font-size: 18px;
  color: #5f6364;
  text-align: center;
}
#gourmet {
  background-color: #dcdfde;
}
#padaria {
  background-color: #1a8acb;
}
#bistro {
  background-color: #fca500;
}
.villa {
  padding: 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  width: 100%;
  min-height: 100%;
}
.villa-img {
  width: 90%;
  height: 200px;
  border-radius: 76px;
  background-color: #c4c4c4;
}

@media screen and (max-width: 1550px){
    .villa-logo{
    width: 355.5px;
    height: 170px;
    }
}
@media screen and (max-width: 1200px){
    .villa-logo{
    width: 251px;
    height: 120px;
    }
}

@media screen and (max-width: 975px){
    #sobre2{
        display: none;
    }
    #slidesobre{
        display: flex;
    }
    .villa{
        display: none;
    }
}

</style>