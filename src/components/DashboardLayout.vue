<template>
    <div class="dashboard">
        <v-navigation-drawer class="fullheight lighten-3" width="256" permanent app fixed>
            <v-list-item>
                <v-list-item-content>
                    <v-list-item-title>
                        Marcellinus Axelle Redo Avila
                    </v-list-item-title>
                    <v-list-item-subtitle>
                        180709749
                    </v-list-item-subtitle>
                </v-list-item-content>
            </v-list-item>

            <v-divider></v-divider>

            <v-list dense nav>
                <v-list-item
                    v-for="item in items"
                    :key="item.title"
                    link
                    tag="router-link"
                    :to="item.to"
                >
                    <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <div class="grey lighten-5 fullheight pa-10">
            <router-view></router-view>
        </div>
    </div>
</template>
<script>
export default {
    name: "Dashboard",
    data() {
    return {
            items: [
                { title: "Dashboard", to: "/" },
                { title: "GD", to: "/gd" },
                { title: "TUGAS", to: "/tgs" },
            ],
        };
    },
};
</script>
<style scoped>
.fullheight {
    min-height: 100vh !important;
}
</style>