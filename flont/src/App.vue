<template>
  <v-app>
    

<v-content>
  <v-content>
    <SideNav/>
  </v-content>

</v-content>
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
import SideNav from './components/SideNav';

export default {
  name: 'App',

  components: {
    SideNav
  },

  data: () => ({
    //
  }),
};
</script>
