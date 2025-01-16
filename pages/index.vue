<template>
  <div>
    <TheHeader />
    <main>
      <HomeHero />
      <HomeAbout />
    </main>
  </div>
</template>

<script>
import HomeHero from "~/components/HomePage/HomeHero.vue";
import HomeAbout from "~/components/HomePage/HomeAbout.vue";

export default {
  components: {
    HomeHero,
    HomeAbout,
  },
};
</script>
