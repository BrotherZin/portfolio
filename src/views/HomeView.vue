<template>
  <div id="home">
    <swiper :options="swiperOption" class="swiper">
      <swiper-slide
        data-aos="fade-in"
        data-aos-duration="1000"
        class="slide"
        style="background-image: url(/portfolio/image/mm2.jpg)"
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

            <vue-typer
              class="typer"
              text="『 앞날을 언제나 밝게 비춰주는 안형진입니다. 』"
              color="red"
            ></vue-typer>
          </div>
        </v-layout>
      </swiper-slide>
      <!-- <swiper-slide class="slide" style="background-image: url(image/top3.jpg)">
        <v-layout fill-height align-center justify-center>
          <div class="slog">언제나 열심히</div>
        </v-layout>
      </swiper-slide>
      <swiper-slide class="slide" style="background-image: url(image/top1.jpg)">
        <v-layout fill-height align-center justify-center>
          <div class="slog">하겠습니다.</div>
        </v-layout>
      </swiper-slide> -->
    </swiper>

    <div id="profile" class="section">
      <div
        id="profile"
        class="header"
        data-aos="fade-down"
        data-aos-delay="200"
      >
        Profile
      </div>

      <v-layout wrap>
        <div style="float: left">
          <img
            src="/portfolio/introduce/s1.jpg"
            class="image"
            data-aos="fade-down"
            data-aos-easing="linear"
            data-aos-duration="1500"
          />
          <div style="float: right">
            <p class="profilehead">Name</p>
            안형진
            <p class="profilehead">Birthday</p>
            1996.06.20
            <p class="profilehead">E-mail</p>
            ahj13k@naver.com
            <p class="profilehead">Address</p>
            경기도 수원시 장안구 정자동
            <p class="profilehead">Phone</p>
            010 - 2061 - 6682
          </div>
          <v-btn
            v-show="scroll > 0"
            fab
            fixed
            dark
            bottom
            v-scroll:#scroll-target="onScroll"
            @click="goTop"
          >
            <v-icon>mdi-menu-up</v-icon>
          </v-btn>
        </div>
      </v-layout>
    </div>
    <div>
      <div class="section">
        <div
          id="license"
          class="header"
          data-aos="fade-left"
          data-aos-delay="200"
        >
          License
        </div>
        <v-layout align-center justify-center>
          <div style="float: left">
            <!-- <div style="display: block; margin: auto; width: auto; height: auto"> -->
            <img
              src="/portfolio/image/license1.png"
              class="image"
              data-aos="fade-left"
              data-aos-delay="550"
            />
          </div>
          <div style="float: ligth">
            <!-- <div style="display: block; margin: auto; width: auto; height: auto"> -->
            <img
              src="/portfolio/image/license2.png"
              class="image"
              data-aos="fade-right"
              data-aos-delay="550"
            />
          </div>
        </v-layout>
      </div>
    </div>
    <div>
      <div class="section">
        <div class="header" data-aos="fade-down" data-aos-delay="200">
          Career
        </div>
        <v-layout align-center justify-center>
          <div id="career">
            <v-card class="mx-auto" max-width="auto">
              <v-img
                src="/portfolio/image/hbm.jpg"
                height="auto"
                width="800"
              ></v-img>

              <v-card-title> 현대사무기기 </v-card-title>

              <v-card-subtitle> Customer Service Engineer </v-card-subtitle>

              <v-card-actions>
                <v-btn color="orange lighten-2" text href="http://www.hbm.kr/">
                  (주)현대사무기기 홈페이지
                </v-btn>
                <v-btn
                  color="orange lighten-2"
                  text
                  href="https://kr.canon/main"
                >
                  캐논 코리아 홈페이지
                </v-btn>
                <v-spacer></v-spacer>

                <v-btn icon @click="show = !show">
                  설명
                  <v-icon>{{
                    show ? "mdi-chevron-up" : "mdi-chevron-down"
                  }}</v-icon>
                </v-btn>
              </v-card-actions>

              <v-expand-transition>
                <div v-show="show">
                  <v-divider></v-divider>

                  <v-card-text>
                    현대사무기기라는 회사에서 Customer Service Engineer로써
                    1년간 근무했으며, Canon Korea에서 주최한 2015 Canon Service
                    Engineer에서 입상한 경력이 있습니다.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </div>
        </v-layout>

        <v-layout class="section" align-center justify-center>
          <div align-center justify-center>
            <v-btn icon href="#home">↑ 맨위로 ↑ </v-btn>
            <v-icon>arrow-u-right-top-bold</v-icon>
            <br />
            <br />
            <br />
          </div>
        </v-layout>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.css";
import AOS from "aos";
import "aos/dist/aos.css";
import { VueTyper } from "vue-typer";
import Vue from "vue";
import VueAnimateOnScroll from "vue-animate-onscroll";

export default {
  name: "home",
  methods: {
    career() {
      this.$router.push("/careerInfo");
    },
  },
  data() {
    return {
      show: false,
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
    Vue.use(VueAnimateOnScroll);
    window.addEventListener("scroll", this.handleScroll);
  },

  components: {
    Swiper,
    SwiperSlide,
    VueTyper,
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
      color: rgb(242, 242, 242);
    }
  }
}
.typer {
  font-weight: normal;
  color: rgb(242, 242, 242);
}

.section {
  padding-top: 300px;
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
  .btn {
    background-color: rgba(67, 102, 174, 0.7);
    font-size: 1.2em;
    color: rgb(255, 255, 255);
  }
}
</style>