<template>
  <v-row
    justify="space-between"
    align="center"
    style="height: 100vh;"
  >
    <v-col
      cols="12"
      sm="6"
    >
      <WaitFormVue />
    </v-col>
    <v-col
      cols="12"
      sm="6"
      class="d-flex justify-center justify-lg-end"
    >
      <img
        src="../../assets/images/hero.png"
        style="width: 70%;"
      />
    </v-col>
  </v-row>
</template>

<script>
import WaitFormVue from '../fragments/WaitForm.vue';
export default {
  components: { WaitFormVue }
}
</script>

<style>
</style>