<template>
  <div>
    <swiper :options="swiperOption" class="swiper">
      <swiper-slide
        data-aos="fade-in"
        data-aos-duration="1000"
        class="slide"
        style="background-image: url(image/mm2.jpg)"
      >
        <v-layout
          data-aos="fade-up"
          data-aos-duration="1000"
          fill-height
          align-center
          justify-center
        >
          <div class="slog" data-aos="fade-up" data-aos-delay="550">
            <br />
            『 언제나 밝게 비춰주는 안형진입니다. 』
            <vue-typer
              class="slog"
              :text="['『 언제나 밝게 비춰주는 안형진입니다. 』', '']"
              :repeat="Infinity"
              :shuffle="false"
              initial-action="typing"
              :pre-type-delay="70"
              :type-delay="70"
              :pre-erase-delay="2000"
              :erase-delay="250"
              erase-style="select-all"
              :erase-on-complete="false"
              caret-animation="smooth"
            ></vue-typer>
          </div>
        </v-layout>
      </swiper-slide>
      <swiper-slide class="slide" style="background-image: url(image/top3.jpg)">
        <v-layout fill-height align-center justify-center>
          <div class="slog">언제나 열심히</div>
        </v-layout>
      </swiper-slide>
      <swiper-slide class="slide" style="background-image: url(image/top1.jpg)">
        <v-layout fill-height align-center justify-center>
          <div class="slog">하겠습니다.</div>
        </v-layout>
      </swiper-slide>
    </swiper>

    <div class="section">
      <div class="header" data-aos="fade-down" data-aos-delay="100">
        안형진을 소개합니다.
      </div>
      <v-layout wrap>
        <div style="float: left">
          <img src="introduce/s1.jpg" class="image" />
          <div style="float: right">
            <p class="profilehead">Name</p>
            안형진
            <p class="profilehead">Birthday</p>
            1996.06.20
            <p class="profilehead">E-mail</p>
            ahj13k@naver.com
            <p class="profilehead">Address</p>
            경기도 수원시 장안구
            <p class="profilehead">Phone</p>
            010 - 2061 - 6682
          </div>
        </div>

        <!-- <v-flex xs4 class="pa-2" data-aos="fade-right">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="introduce/s1.jpg" class="image" />
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-down" data-aos-delay="100">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="image/top2.jpg" class="image" />
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-left" data-aos-delay="200">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="image/top3.jpg" class="image" />
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-right">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="image/top3.jpg" class="image" />
          </v-responsive>
        </v-flex> -->
        <!-- <v-flex xs4 class="pa-2" data-aos="fade-up" data-aos-delay="100">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="image/top2.jpg" class="image" />
          </v-responsive>
        </v-flex>
        <v-flex xs4 class="pa-2" data-aos="fade-left" data-aos-delay="200">
          <v-responsive :aspect-ratio="1 / 1">
            <img src="image/top1.jpg" class="image" />
          </v-responsive>
        </v-flex> -->
      </v-layout>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.css";
import AOS from "aos";
import "aos/dist/aos.css";
import { VueTyper } from "vue-typer";

export default {
  name: "home",
  data() {
    return {
      swiperOption: {
        loop: true,
        autoplay: {
          delay: 1000,
        },
      },
    };
  },
  mounted() {
    AOS.init();
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<style scoped lang="less">
.swiper {
  height: 100vh;
  .slide {
    background-size: cover;
    background-position: center center;
    .slog {
      font-size: 30px;
      font-weight: normal;
      color: yellow;
    }
  }
}

.section {
  width: 1190px;
  margin: 0 auto;

  .header {
    text-align: center;
    font-size: 40px;
    font-weight: bold;
  }
  .image {
    width: 70%;
    height: 100%;
    object-fit: cover;
  }
  .profilehead {
    font-weight: bold;
    font-size: 1.8em;
  }
}
</style>