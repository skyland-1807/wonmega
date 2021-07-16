<template>
  <v-app>
    <v-app-bar app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer">
      <v-list nav dense>
        <v-list-item link>
          <v-list-item-title>Foo</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-title>Bar</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-title>Shit</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container fluid>
        <!--<router-view></router-view>-->
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
  }),
  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
