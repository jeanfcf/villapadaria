<template>
  <div id="slidesobre">
    <swiper :options="swiperOption">
      <swiper-slide>
        <div id="slidesobre1" class="slide">
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
            <img class="villa-slide-logo" src="../../assets/sobre/villa_gourmet.png" alt="gourmet" />
            <div class="villa-slide-img"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div id="slidesobre2" class="slide">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
            <img class="villa-slide-logo" src="../../assets/sobre/villa_padaria.png" alt="gourmet" />
            <div class="villa-slide-img"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div id="slidesobre3" class="slide">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis vel quas, aperiam harum aliquam cupiditate saepe aspernatur commodi ad possimus placeat tenetur quidem maxime inventore. Unde, nesciunt. Unde, eligendi earum!</p>
            <img class="villa-slide-logo" src="../../assets/sobre/villa_bistro.png" alt="gourmet" />
            <div class="villa-slide-img"></div>
        </div>
      </swiper-slide>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        autoplay: true,
        slidesPerView: 1,
        loop: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  }
};
</script>

<style scoped>
#slidesobre1 {
  background-color: #dcdfde;
}
#slidesobre2 {
  background-color: #1a8acb;
}
#slidesobre3 {
  background-color: #fca500;
}
#slidesobre{
  display: flex;
  height: 100%;
  align-items: center;
}

#slidesobre p {
    font-size: 24px;
  color: #5f6364;
  padding-left: 10%;
  padding-right: 10%;
  text-align: center;
}
.slide {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  background-position: center;
  background-size: cover;
  min-height: 100vh;
  width: 100vw;
  padding: 5%;
}

.villa-slide-img {
  width: 90%;
  height: 250px;
  border-radius: 76px;
  background-color: #c4c4c4;
}

@media screen and (max-width: 700px){

  .villa-slide-logo{
    width: 355.5px;
    height: 170px;
  }

  .villa-slide-img{
    height: 200px;
  }
  
}

@media screen and (max-width: 500px){

  #slidesobre p {
    font-size: 20px;

}

  .villa-slide-logo{
       width: 251px;
    height: 120px;
  }

  .villa-slide-img{
    height: 150px;
  }
  
}
@media screen and (max-width: 374px){

  #slidesobre p {
    font-size: 14px;

}
.villa-slide-logo{
       width: 198.75px;
    height: 95px;
  }
}

@media screen and (max-height: 420px){
   #slidesobre p {
    margin-bottom: 5%;

}
.villa-slide-logo{
margin-bottom: 5%;
  
}
}
</style>