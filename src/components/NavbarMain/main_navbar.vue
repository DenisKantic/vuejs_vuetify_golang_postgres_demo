<template>
  <v-app>
    <v-app-bar absolute color="gray accent-80" dark>
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>BLOG APP</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <!-- Navigation Drawer -->
    <v-navigation-drawer v-model="drawer" app>
      <button @click="toggleDrawer" class="text-h5">Close</button>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">Application</v-list-item-title>
          <v-list-item-subtitle>subtext</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :to="item.to" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid>
        <!-- Your main content goes here -->
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "Home", icon: "mdi-view-dashboard", to: "/" },
        { title: "Dashboard", icon: "mdi-image", to: "/dashboard" },
        { title: "About", icon: "mdi-help-box" },
      ],
      drawer: false, // Controls visibility of the drawer
    };
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer; // Toggle the drawer visibility
    },
  },
};
</script>
