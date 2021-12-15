<template>
  <section class="cars">
    <h2 class="title">Viaturas recentes</h2>
    <!-- <Car
        model="Renault Captur"
        version="E-Tech Híbrido Plug-In Intens 2021"
      />
      <Car
        model="Renault Captur"
        version="E-Tech Híbrido Plug-In Intens 2021"
      />
      <Car
        model="Renault Captur"
        version="E-Tech Híbrido Plug-In Intens 2021"
      />
      <Car
        model="Renault Captur"
        version="E-Tech Híbrido Plug-In Intens 2021"
      /> -->
    <swiper
      :slides-per-view="4"
      :space-between="16"
      :breakpoints="breakpoints"
      :allowTouchMove="false"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide
        ><Car
          model="Renault Captur"
          version="E-Tech Híbrido Plug-In Intens 2021"
        />
      </swiper-slide>
      <swiper-slide
        ><Car
          model="Renault Captur"
          version="E-Tech Híbrido Plug-In Intens 2021"
        />
      </swiper-slide>
      <swiper-slide
        ><Car
          model="Renault Captur"
          version="E-Tech Híbrido Plug-In Intens 2021"
        />
      </swiper-slide>
      <swiper-slide
        ><Car
          model="Renault Captur"
          version="E-Tech Híbrido Plug-In Intens 2021"
        />
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import Car from "@/components/Car.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
export default {
  name: "CarsList",
  components: {
    Car,
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      breakpoints: {
        320: {
          slidesPerView: "'auto'",
          /* grabCursor: "true", */
          allowTouchMove: "true",
        },
        /* 480: {
          slidesPerView: "'auto'",
          /* grabCursor: "true",
          allowTouchMove: "true",
        }, */
        640: {
          slidesPerView: 4,
          /* grabCursor: "false", */
          /* allowTouchMove: "false", */
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  margin: 0 64px 112px;
}
@media only screen and (max-width: 600px) {
  section {
    margin: 0 16px 80px;
  }
}
.title {
  font-family: "Mont Semibold";
  font-size: clamp(18px, 1.46vw, 28px);
  line-height: 1.3;
  margin: 0 0 24px;
}
.cars_wrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  margin: 0 64px;
}
@media only screen and (max-width: 600px) {
  .swiper-slide {
    width: 90%;
  }
}
</style>
