<template>
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="(slide, index) in slides" :key="index">
        <div class="hidden">
          <p class="txt">
            {{ slide.title }}
          </p>
        </div>
        <img :src="slide.image" :alt="slide.title" />
      </div>
    </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import Swiper from "swiper";
import { Autoplay } from "swiper/modules";
import "swiper/swiper-bundle.css";

const props = defineProps({
  slides: {
    type: Array,
    required: true,
  },
});

const swiperInstance = ref(null);

onMounted(() => {
  swiperInstance.value = new Swiper(".swiper", {
    modules: [Autoplay],
    loop: true,
    slidesPerView: 3,
    spaceBetween: 28,
    effect: "coverflow",
    centeredSlides: true,
    autoplay: {
      delay: 5000,
      disableOnInteraction: false,
    },
  });
});

defineExpose({
  swiperInstance,
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
  position: relative;
  overflow: hidden;
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

.hidden {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: hsla(229, 100%, 66%, 0.7);
  transition: 0.4s;
  opacity: 0;
}

.txt {
  color: white;
  font-size: 24px;
  font-family: var(--medium);
}

.swiper :deep(.swiper-slide-active:hover) .hidden {
  opacity: 1;
}
</style>
