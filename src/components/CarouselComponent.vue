<script setup lang="ts">
import CardComponent from "./CardComponent.vue";
import {Swiper, SwiperSlide} from "swiper/vue";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css";

const onSwiper = (swiper: any) => {
   console.log(swiper);
};
const onSlideChange = () => {
   console.log("slide change");
};
</script>
<template>
   <div>
      <Swiper
         :centerInsufficientSlides="true"
         slidesPerView="auto"
         :spaceBetween="16"
         :enabled="true"
         :observer="true"
         :observeParents="true"
         :centeredSlides="true"
         :parallax="true"
         @swiper="() => onSwiper()"
         @slideChange="onSlideChange">
         <SwiperSlide
            v-for="item in 10"
            :key="item"
            v-slot="{isActive}">
            <CardComponent>{{ isActive ? item : "InActive" }}</CardComponent>
         </SwiperSlide>
      </Swiper>
   </div>
</template>

<style scoped lang="scss">
.swiper {
   .swiper-wrapper {
      .swiper-slide {
         width: 150px;
         height: auto;
      }
   }
}
</style>
