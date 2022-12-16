<template>
  <v-container class="body">
    <h1 class="text-h4 text-sm-h3 text-md-h2 font-weight-regular">About Us</h1>
    <Section1Vue />
  </v-container>
</template>

<script>
import Section1Vue from "../components/about/Section1.vue";
export default {
  components: { Section1Vue },
};
</script>

<style>
.body {
  margin-top: 30vh;
}
</style>
