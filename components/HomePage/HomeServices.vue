<template>
  <div class="wrap">
    <div class="container">
      <div class="liner">
        <h4 class="section__title">Services</h4>

        <p class="txt">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda
          fugit accusantium enim fugiat debitis assumenda fugit accusantium enim
          fugiat debitis
        </p>
      </div>
    </div>

    <div class="slider">
      <Swiper :slides="slides" />
    </div>
  </div>
</template>

<script setup>
const slides = [
  {
    title: "Frontend",
    image: "/assets/img/serv-1.jpg",
  },
  {
    title: "Backend",
    image: "/assets/img/serv-2.jpg",
  },
  {
    title: "Game development",
    image: "/assets/img/serv-3.jpg",
  },
  {
    title: "Graphic design",
    image: "/assets/img/serv-4.jpg",
  },
];
</script>

<style scoped>
.liner {
  padding-bottom: 40px;
}
.txt {
  font-size: 24px;
  max-width: 80%;
  display: flex;
}
.swiper {
  border-block: 1px solid #ebebeb;
  padding: 40px 0;
}
.slider {
  padding-bottom: 80px;
}
</style>
