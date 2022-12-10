<template>
  <v-card flat width="450" max-width="100%">
    <v-card-title
      class="colorText text-h5 text-md-h4 text-lg-h2 font-weight-bold"
      >coming soon</v-card-title
    >
    <v-card-subtitle class="text-grey-darken-3 font-weight-bold"
      >Get notified when we launch 🚀🚀🚀</v-card-subtitle
    >

    <v-card-text class="d-flex mt-5">
      <v-row>
        <v-col cols="12">
          <v-text-field
            density="comfortable"
            variant="outlined"
            label="Your name"
            placeholder="Your name"
            prepend-inner-icon="mdi-account"
            class="mr-2"
            hide-details
            color="dark"
          />
        </v-col>
        <v-col cols="12">
          <v-text-field
            density="comfortable"
            variant="outlined"
            label="Email"
            placeholder="example@gmail.com"
            prepend-inner-icon="mdi-at"
            class="mr-2"
            hide-details
            color="dark"
          />
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {};
</script>

<style scoped>
.colorText {
  background: -webkit-linear-gradient(45deg, #ff4f98, #727aff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  line-height: 1em;
}
.emoji {
  color: initial !important;
}
</style>