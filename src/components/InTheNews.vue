<template>
    <v-container grid-list-lg>
        <v-layout row>
            <v-flex xs12 class="text-xs-center display-1 font-weight-black my-5">In the News</v-flex>
        </v-layout>
        <v-layout row wrap>
            <v-flex xs12 sm12 md4 v-for="(item, index) in news" :key="index">
                <v-card>
                    <v-img :src="image" height="300px"></v-img>
                    <v-card-title>
                        <div>{{item.title}}</div>
                    </v-card-title>
                    <v-card-text>
                        <div>{{item.text}}</div>
                    </v-card-text>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'InTheNews',
    data() {
        return {
            image: require('@/assets/hh-home.jpg'),
            news: [{
                title: 'Story 1',
                text: 'Retired teacher and certified Nebraska Master Naturalist LeDoux is channeling her expertise on native ecosystems and habitat conservation into volunteer work at Heron Haven, a wetland sanctuary in northwest Omaha that offers free, daily trail access (flat and full of photo opportunities) from sunrise to sunset.'
            },{
                title: 'Story 2',
                text: 'Retired teacher and certified Nebraska Master Naturalist LeDoux is channeling her expertise on native ecosystems and habitat conservation into volunteer work at Heron Haven, a wetland sanctuary in northwest Omaha that offers free, daily trail access (flat and full of photo opportunities) from sunrise to sunset.'
            },{
                title: 'Story 3',
                text: 'Retired teacher and certified Nebraska Master Naturalist LeDoux is channeling her expertise on native ecosystems and habitat conservation into volunteer work at Heron Haven, a wetland sanctuary in northwest Omaha that offers free, daily trail access (flat and full of photo opportunities) from sunrise to sunset.'
            }]
        }
    }
}
</script>

<style scoped>

</style>

