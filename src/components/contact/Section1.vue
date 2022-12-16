<template>
  <v-row class="mt-12" justify="space-between">
    <v-col cols="12" sm="6">
      <v-row justify="space-between" align="start" dense>
        <v-col cols="12">
          <v-card flat variant="outlined">
            <v-card-title class="text-uppercase">ADDRESS</v-card-title>
            <v-card-text>
              20 Premabri Street, off Wogu street, Obio/Akpor, Port harcourt,
              Rivers state, Nigeria
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card flat variant="outlined">
            <v-card-title class="text-uppercase">Email</v-card-title>
            <v-card-text> Customer service: help@oymo.ng </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card flat variant="outlined">
            <v-card-title class="text-uppercase">phone</v-card-title>
            <v-card-text>
              +234 8071 657 43
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="12" sm="5" class="d-flex justify-center">
      <v-card flat>
        <ContactFormVue />
      </v-card>
    </v-col>
  </v-row>
</template>
  
  <script>
import ContactFormVue from "../fragments/ContactForm.vue";
export default {
  components: { ContactFormVue },
};
</script>
  