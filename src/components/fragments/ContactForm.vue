<template>
  <v-row dense>
    <v-col cols="12" sm="6">
      <v-text-field
        label="Email"
        hide-details
        variant="outlined"
        placeholder="example@mail.com"
        prepend-inner-icon="mdi-account"
        />
    </v-col>
    <v-col cols="12" sm="6">
        <v-text-field
        label="Name"
        hide-details
        variant="outlined"
        prepend-inner-icon="mdi-at"
        placeholder="Your special name"
      />
    </v-col>
    <v-col cols="12">
      <v-textarea label="Feedback" variant="outlined"></v-textarea>
    </v-col>
    <v-col cols="12" class="text-right">
        <v-btn color="#FF4040" class="text-white text-capitalize" flat>Submit</v-btn>
    </v-col>
  </v-row>
</template>

<script>
export default {};
</script>

<style>
</style>