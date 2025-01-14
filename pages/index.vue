<template>
    <div>
        <TheHeader />
        <main>
            <HomeHero />
        </main>
    </div>
</template>

<script>
import HomeHero from '~/components/HomePage/HomeHero.vue';
export default {
    components: {
        HomeHero
    }
}
</script>