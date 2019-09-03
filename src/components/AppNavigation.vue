<template>
    <span>
        <v-navigation-drawer app v-model="drawer" class="brown lighten-2" dark disable-resize-watcher>
            <v-list nav>
                <v-list-item v-for="(item, index) in items" :key="index" link>
                    <v-list-item-content>
                        <v-list-item-title>
                            {{ item.title }}
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>

        <!-- app prop is used to dynamically adjust content sizing -->
        <v-app-bar app color="brown darken-4" dark>
            <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>

            <v-toolbar-title>{{ appTitle }}</v-toolbar-title>

            <v-toolbar-items>
                <v-btn text class="hidden-sm-and-down">Menu</v-btn>
                <v-btn text class="hidden-sm-and-down">How It Works</v-btn>
            </v-toolbar-items>
            
            <v-spacer class="hidden-sm-and-down"></v-spacer>

            <v-toolbar-items>
                <v-btn text class="hidden-sm-and-down">SIGN IN</v-btn>
                <v-btn color="brown lighten-3" class="hidden-sm-and-down">JOIN</v-btn>
            </v-toolbar-items>
            
        </v-app-bar>
    </span>
</template>
    
<script>
export default {
    name: 'AppNavigation',
    data() {
        return {
            appTitle: 'Meal Prep',
            drawer: false,
            items: [
                { title: 'Menu' },
                { title: 'Sign In' },
                { title: 'Join' }
            ]
        };
    }
};
</script>

<style scoped>
</style>