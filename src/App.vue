<template>
  <v-app>
    <AppbarVue />
    <v-main>
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
    </v-main>
    <FooterVue />
  </v-app>
</template>

<script>
import AppbarVue from "./components/Appbar.vue";
import FooterVue from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    AppbarVue,
    FooterVue,
  },
};
</script>


<style>
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