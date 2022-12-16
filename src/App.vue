<template>
  <v-app>
    <AppbarVue />
    <v-main>
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
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


<style>
@import url("https://fonts.googleapis.com/css2?family=Fira+Code&display=swap");
* {
  font-family: "Fira Code", monospace !important;
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.8s;
  transition-property: opacity;
  transition-timing-function: ease-in-out;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
}
</style>