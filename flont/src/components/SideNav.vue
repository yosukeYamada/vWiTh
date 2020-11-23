<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer">
      <v-list-item>
        <v-list-item-title class="title"> vWiTh </v-list-item-title>
        <v-btn icon>
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>
      <v-divider />
      <v-list nav>
        <v-list-item v-for="menu in menus" :key="menu.title" :to="menu.url">
          <v-list-item-icon>
            <v-icon>{{ menu.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ menu.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <!-- アプリケーションバー -->
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>

    <v-footer app>
      <!-- フッター -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    drawer: false,
    menus: [
      { title: "Home", icon: "mdi-web", url: "/" },
      { title: "household", icon: "mdi-dots-vertical", url: "/household" },
      { title: "About", icon: "mdi-information-variant", url: "/about" },
    ],
  }),
};
</script>