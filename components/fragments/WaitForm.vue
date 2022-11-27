<template>
  <v-card flat>
    <v-card-title class="colorText text-h5 text-md-h4 text-lg-h2 font-weight-bold">coming soon</v-card-title>
    <v-card-subtitle class="grey--text text--darken-3 font-weight-bold">Get notified when we launch 🚀🚀🚀</v-card-subtitle>

    <v-card-text class="d-flex mt-5">
      <v-text-field
        dense
        placeholder="Your name"
        prepend-inner-icon="mdi-account-outline"
        class="mr-2"
        hide-details
        color="dark"
      />
      <v-text-field
        dense
        placeholder="Email"
        prepend-inner-icon="mdi-at"
        class="ml-2"
        hide-details
        color="dark"
      />
    </v-card-text>

    <v-card-actions>
      <v-btn dark depressed rounded class="px-8 text-capitalize">
        Join wait list
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {

}
</script>

<style>
.colorText {
  background: -webkit-linear-gradient(45deg, #FF4F98, #727AFF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.emoji {
  color: initial !important;
}
</style>