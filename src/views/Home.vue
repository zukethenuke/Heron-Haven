<template>
  <span>
    <home-carousel></home-carousel>
    <in-the-news></in-the-news>
  </span>
</template>

<script>
// @ is an alias to /src
import HomeCarousel from '@/components/HomeCarousel.vue';
import InTheNews from '@/components/InTheNews.vue';

export default {
    name: 'home',
    components: {
        HomeCarousel,
        InTheNews
    }
};
</script>
