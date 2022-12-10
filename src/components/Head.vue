<template>
  <v-container>
    <v-row justify="space-between" align="center" style="height: 80vh">
      <v-col cols="12" sm="6">
        <WaitFormVue />
      </v-col>
      <v-col cols="12" sm="6" class="d-none d-sm-flex justify-center justify-lg-end">
        <img src="../assets/images/hero.png" style="width: 70%" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import WaitFormVue from "./fragments/WaitForm.vue";
export default {
  name: "HelloWorld",
  components: {
    WaitFormVue,
  },
};
</script>
