<template>
  <span>
    <home-carousel></home-carousel>
  </span>
</template>

<script>
// @ is an alias to /src
import HomeCarousel from '@/components/HomeCarousel.vue';

export default {
    name: 'home',
    components: {
        HomeCarousel
    }
};
</script>
