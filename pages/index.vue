<template>
  <div>
    <TheHeader />
    <main>
      <HomeHero />
      <HomeAbout />
      <HomeServices />
      <HomePortfolio />
      <HomeWhy />
      <HomeForm />
    </main>
    <TheFooter />
  </div>
</template>

<script>
import HomeHero from "~/components/HomePage/HomeHero.vue";
import HomeAbout from "~/components/HomePage/HomeAbout.vue";
import HomeServices from "~/components/HomePage/HomeServices.vue";
import HomePortfolio from "~/components/HomePage/HomePortfolio.vue";
import HomeWhy from "~/components/HomePage/HomeWhy.vue";
import HomeForm from "~/components/HomePage/HomeForm.vue";

export default {
  components: {
    HomeHero,
    HomeAbout,
    HomeServices,
    HomePortfolio,
    HomeWhy,
    HomeForm,
  },
};
</script>
