<template>
  <div>
    <TheHeader />
    <main>
      <HomeHero />
      <HomeAbout />
      <HomeServices />
      <HomePortfolio />
    </main>
  </div>
</template>

<script>
import HomeHero from "~/components/HomePage/HomeHero.vue";
import HomeAbout from "~/components/HomePage/HomeAbout.vue";
import HomeServices from "~/components/HomePage/HomeServices.vue";
import HomePortfolio from "~/components/HomePage/HomePortfolio.vue";

export default {
  components: {
    HomeHero,
    HomeAbout,
    HomeServices,
    HomePortfolio,
  },
};
</script>
