<template>
  <div id="slide">
    <swiper :options="swiperOption" id="swiper">
      <swiper-slide>
        <div id="slide1" class="slide" :style="{ backgroundImage: 'url(' + img[0] + ')' }"></div>
      </swiper-slide>
      <swiper-slide>
        <div id="slide2" class="slide" :style="{ backgroundImage: 'url(' + img[0] + ')' }"></div>
      </swiper-slide>
      <swiper-slide>
        <div id="slide3" class="slide" :style="{ backgroundImage: 'url(' + img[0] + ')' }"></div>
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
      img: [require("../../assets/home/slide/croissant.svg")],
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
#slide {
  display: flex;
  height: 100%;
  align-items: center;
}
.slide {
  background-position: center;
  background-size: cover;
  height: 300px;
  width: 100vw;
}

@media screen and (max-width: 600px) {
  .slide {
    height: 250px;
  }
}
@media screen and (max-height: 567px) {
  .slide {
    height: 150px;
  }
}
</style>