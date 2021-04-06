<template>
  <v-navigation-drawer app>
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="title">
          Application
        </v-list-item-title>
        <v-list-item-subtitle>
          subtext
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list nav>
      <v-list-item
        v-for="item in items"
        :key="item.title"
        link
        @click="routePush(item.route)"
      >
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
import router from "@/router/index.js";
export default {
  data() {
    return {
      items: [
        { title: "Home", icon: "mdi-view-dashboard", route: "/home" },
        { title: "About", icon: "mdi-image", route: "/about" },
      ],
      right: null,
    };
  },
  methods: {
    routePush: function(path) {
      router.push(path);
    },
  },
};
</script>
