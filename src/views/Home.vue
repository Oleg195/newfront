<template >
  <h2>Update of News</h2>

  <swiper
    :modules="modules"
    :slides-per-view="3"
    :space-between="50"
    :autoplay="{
      delay: 2000,
      disableOnInteraction: false,
    }"
    :breakpoints="{
      // when window width is >= 320px
      200: {
        slidesPerView: 1,
        spaceBetween: 10,
      },
      320: {
        slidesPerView: 1,
        spaceBetween: 10,
      },
      // when window width is >= 480px
      480: {
        slidesPerView: 2,
        spaceBetween: 30,
      },
      // when window width is >= 640px
      640: {
        slidesPerView: 4,
        spaceBetween: 40,
      },
    }"
    :pagination="{
      clickable: true,
    }"
    navigation
  >
    <swiper-slide>
      <div class="numbertext">1 / 8</div>
      <img src="../views/images/img1.jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">2 / 8</div>
      <img src="../views/images/img2.jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">3 / 8</div>
      <img src="../views/images/img3.jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">4 / 8</div>
      <img src="../views/images/img4.jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">5 / 8</div>
      <img src="../views/images/img5.jfif" style="width: 100%" />
      <div class="text">The Best Electronics Store</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">6 / 8</div>
      <img src="../views/images/Снимок экрана (13).png" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">7 / 8</div>
      <img src="../views/images/Снимок экрана (7).jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
    <swiper-slide>
      <div class="numbertext">8 / 8</div>
      <img src="../views/images/img2.jpg" style="width: 100%" />
      <div class="text">New sources of supply</div>
    </swiper-slide>
  </swiper>


</template>

<script>
import { Autoplay, Pagination, Navigation, Scrollbar, A11y } from "swiper";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Navigation, Pagination, Scrollbar, A11y],
    };
  },
};

</script>

<style scoped>
* {
  box-sizing: border-box;
 
}

img {
  vertical-align: middle;
  height: 400px;
 
}
/* Caption text */
.text {
  color: #302a64;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;

;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #240b0b;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}



/* On smaller screens, decrease text size */
@media only screen and (max-width: 320px) {
  .text {
    font-size: 11px;
  }
}

.swiper-slide{   margin-bottom: 47px;

    box-shadow: 8px 7px 5px 3px red, 
                3px 5px 4px 6px blue,
                3px 5px 5px 6px orange;
}
swiper{}
h2{text-align: center;
color:#302a64;
text-transform:uppercase;

}
</style>