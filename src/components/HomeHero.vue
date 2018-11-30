<template>
    <v-container fluid fill-height class="home-hero" style="max-height: 100vh;">
        <!-- <v-layout justify-center align-center column pa-5>
            <v-btn fab class="mt-5 brown darken-4">
            <v-icon large color="white">expand_more</v-icon>
            </v-btn>
        </v-layout> -->
        <v-carousel
            delimiter-icon="stop"
            prev-icon="mdi-arrow-left"
            next-icon="mdi-arrow-right">
            <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
            ></v-carousel-item>
        </v-carousel>
    </v-container>
</template>

<script>
export default {
    name: 'HomeHero',
    data() {
        return {
            items: [{
                src: require('@/assets/hh-home.jpg')
            },{
                src: require('@/assets/hh-boardwalk.jpg')
            },{
                src: require('@/assets/hh-home.jpg')
            },{
                src: require('@/assets/hh-home.jpg')
            },{
                src: require('@/assets/hh-home.jpg')
            }]
        }
    }
};
</script>

<style scoped>
/* .home-hero {
    background: url('../assets/hh-home.jpg');
    background-size: cover;
    width: 100%;
    height: 100%;
} */
</style>
