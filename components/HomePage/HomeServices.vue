<template>
  <div class="wrap">
    <div class="anchor" id="services"></div>
    <div class="container">
      <div class="liner">
        <h4 class="section__title">Services</h4>

        <div class="header">
          <p class="txt">
            Throughout my career, I’ve worked on a wide range of projects, from
            elegant landing pages to complex e-commerce platforms. My focus has
            always been on delivering clean, efficient, and user-friendly
            solutions that meet both client and user needs.
          </p>

          <div class="buttons">
            <button @click="prevSlide" class="prev">
              <Icon icon="material-symbols:chevron-left-rounded" />
            </button>
            <button @click="nextSlide" class="next">
              <Icon icon="material-symbols:chevron-right-rounded" />
            </button>
          </div>
        </div>
      </div>
    </div>

    <div class="slider">
      <Swiper ref="swiperRef" :slides="slides" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const slides = [
  {
    title: "Landing pages",
    image: "/assets/img/serv-1.jpg",
  },
  {
    title: "Catalog websites",
    image: "/assets/img/serv-2.jpg",
  },
  {
    title: "E-commerce platforms",
    image: "/assets/img/serv-3.jpg",
  },
  {
    title: "Crm systems",
    image: "/assets/img/serv-4.jpg",
  },
];

const swiperRef = ref(null);

function nextSlide() {
  if (swiperRef.value && swiperRef.value.swiperInstance) {
    swiperRef.value.swiperInstance.slideNext();
  }
}

function prevSlide() {
  if (swiperRef.value && swiperRef.value.swiperInstance) {
    swiperRef.value.swiperInstance.slidePrev();
  }
}
</script>

<style scoped>
.liner {
  padding-bottom: 40px;
}

.txt {
  font-size: 18px;
  max-width: 95%;
  display: flex;
}

.swiper {
  border-block: 1px solid #ebebeb;
  padding: 40px 0;
}

.slider {
  margin-bottom: -1px;
}

.header {
  display: grid;
  grid-template-columns: 7fr 3fr;
}

.buttons {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 8px;
  padding-right: 32px;
}

.buttons button {
  border: 1px solid var(--blue);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.buttons button svg {
  width: 24px;
  height: 24px;
}

.buttons :deep(path) {
  fill: var(--blue);
}
@media (max-width: 1023px) {
  .liner {
    padding: 0 12px 32px 12px;
    border-block: 0;
  }
  .buttons {
    display: none;
  }
  .header {
    grid-template-columns: repeat(1, 1fr);
  }
  .txt {
    font-size: 14px;
  }
}
</style>
