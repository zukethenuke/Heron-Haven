<template>
    <span>
        <v-navigation-drawer app v-model="drawer" class="brown lighten-2" dark disable-resize-watcher>
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-tile :key="index" :to="item.route">
                        <v-list-tile-content>
                            {{item.title}}
                        </v-list-tile-content>
                    </v-list-tile>
                    <v-divider :key="`divider-${index}`"></v-divider>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-toolbar app color="brown darken-4" dark>
            <v-toolbar-side-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-toolbar-side-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>

            <router-link to="/">
                <v-toolbar-title>{{appTitle}}</v-toolbar-title>
            </router-link>

            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-menu class="hidden-sm-and-down" open-on-hover nudge-bottom="38">
                <v-btn
                    slot="activator"
                    color="brown lighten-3"
                    dark>Friends of Heron Haven
                </v-btn>
                <v-list>
                    <v-list-tile
                        v-for="(item, index) in friends"
                        :key="index"
                        to="/">
                        <v-list-tile-title>{{item.title}}</v-list-tile-title>
                    </v-list-tile>
                </v-list>
            </v-menu>
            <v-btn flat class="hidden-sm-and-down" to="/map">Map</v-btn>
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn flat class="hidden-sm-and-down" to="/sign-in">SIGN IN</v-btn>
            <v-btn color="brown lighten-3" class="hidden-sm-and-down" to="/join">JOIN</v-btn>
        </v-toolbar>
    </span>
</template>

<script>
export default {
    name: 'AppNavigation',
    data() {
        return {
            appTitle: 'Heron Haven',
            drawer: false,
            items: [
                { title: 'Home', route: '/' },
                { title: 'Sign In', route: '/sign-in' },
                { title: 'Join', route: '/join' }
            ],
            friends: [
                { title: 'Information' },
                { title: 'Membership Application' },
                { title: 'Contact us' }
            ]
        };
    }
};
</script>

<style scoped>
a {
    color: white;
    text-decoration: none;
}
</style>