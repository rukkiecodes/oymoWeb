<template>
  <v-container class="my-16">
    <v-row justify="space-between" align="center">
      <v-col cols="12" sm="5" class="d-flex justify-center justify-lg-start">
        <v-card width="100%" flat>
          <v-card-text>
            <img src="../../assets/images/all.png" style="width: 100%" />
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" sm="7">
        <v-card flat>
          <v-card-text class="text-h5 text-sm-h4 font-weight-medium pb-0"
            >Ready to take your dating life to the next level?</v-card-text
          >
          <v-card-text
            class="title text-h5 text-sm-h4 font-weight-medium mt-0 pt-0"
            >Download the Oymo app</v-card-text
          >
          <v-card-text class="py-0">
            <v-card-actions class="pl-0 d-flex justify-start align-start">
              <v-card width="150" class="ma-0 pa-0" flat>
                <img src="../../assets/images/qr.jpeg" style="width: 100%" />
              </v-card>
              <span class="text-body-2 font-weight-medium mt-4"
                >Scan the QR code with your phone camera to download the Oymo
                app.</span
              >
            </v-card-actions>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
* {
  line-height: initial !important;
}
.title {
  color: #ff4040;
}
</style>