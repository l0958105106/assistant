<template>
  <v-app>
    <AppBar />
    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>
<script>
import AppBar from "@/components/AppBar.vue";

export default {
  components: {
    AppBar,
  },
};
</script>
