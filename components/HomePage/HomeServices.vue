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
  </div>
</template>

<script setup>
import { ref } from "vue";

const tabs = ref([
  { title: "Frontend", image: "/assets/img/serv-1.jpg" },
  { title: "Backend", image: "/assets/img/serv-2.jpg" },
  { title: "Game development", image: "/assets/img/serv-3.jpg" },
  { title: "Graphic design", image: "/assets/img/serv-4.jpg" },
]);

const activeTab = ref(0);
</script>

<style scoped>
.txt {
  font-size: 24px;
  max-width: 80%;
  display: flex;
}
</style>
