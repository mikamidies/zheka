<template>
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="(slide, index) in slides" :key="index">
        <img :src="slide.image" :alt="slide.title" />
      </div>
    </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import Swiper from "swiper";
import { Zoom } from "swiper/modules";
import "swiper/swiper-bundle.css";

const props = defineProps({
  slides: {
    type: Array,
    required: true,
  },
});

onMounted(() => {
  new Swiper(".swiper", {
    modules: [Zoom],
    zoom: true,
    loop: true,
    slidesPerView: 3,
    spaceBetween: 28,
    effect: "coverflow",
    centeredSlides: true,
    pagination: {
      el: ".swiper-pagination",
      clickable: true,
    },
    navigation: {
      nextEl: ".swiper-button-next",
      prevEl: ".swiper-button-prev",
    },
  });
});
</script>

<style scoped>
.swiper {
  width: 100%;
}

.swiper-slide {
  text-align: center;
  transition: 0.4s;
  border-radius: 10px;
}

.swiper-slide img {
  width: 100%;
  height: 360px;
  object-fit: cover;
  border-radius: 10px;
}

.swiper :deep(.swiper-slide-active) {
  transform: scale(1.1);
  z-index: 99;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}
</style>
