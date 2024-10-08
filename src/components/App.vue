<template>
  <v-app>
    <component :is="navbarComponent" />
    <router-view />

    <v-main> </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import Navbar from "./NavbarMain/main_navbar.vue";
import DashboardNavbar from "./dashboard/navigation/dashboard_navbar.vue";

export default Vue.extend({
  name: "App",

  components: {
    Navbar,
    DashboardNavbar,
  },

  computed: {
    navbarComponent() {
      // determine which navbar to show based on the current route
      if (this.$route.path.startsWith("/dashboard")) {
        return "DashboardNavbar";
      }
      return "Navbar";
    },
  },
});
</script>
