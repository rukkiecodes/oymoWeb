<template>
  <v-app>
    <AppbarVue />
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import AppbarVue from "./components/Appbar.vue";
export default {
  name: "App",
  components: {
    AppbarVue,
  },
};
</script>
