<template>
  <v-app>
    <v-app-bar>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer">
      Drawer is here
    </v-navigation-drawer>
  </v-app>
</template>

<script>
import Vue from "vue";
export default Vue.extend({
  data: () => ({
    drawerOpen: null,
  }),

  computed: {
    drawer: {
      get: function() {
        return this.drawerOpen;
      },
      set: function(value) {
        console.log("%c set", "color: red");
        console.trace("set trace");
        this.drawerOpen = value;
      },
    },
  },
});
</script>
