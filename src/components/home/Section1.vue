<template>
  <v-container class="my-16">
    <v-row justify="space-between" align="center">
      <v-col cols="12" sm="4" class="d-flex justify-center justify-lg-start">
        <v-card width="400" flat>
          <v-card-text>
            <img src="../../assets/images/match.png" style="width: 100%" />
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4" class="d-flex justify-center">
        <v-progress-circular
          :rotate="360"
          :size="200"
          :width="15"
          :model-value="20"
          color="#ff4040"
        >
          <div class="d-flex flex-column justify-center align-center">
            <span class="text-h6 text-uppercase">Over</span>
            <span class="title text-h3 font-weight-bold">{{
              (2000).toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
            }}+</span>
            <span class="text-body-2 text-uppercase font-weight-medium"
              >Match per day</span
            >
          </div>
        </v-progress-circular>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card flat>
          <v-card-title class="title text-uppercase text-body-1"
            >Quick match up</v-card-title
          >
          <v-card-text class="text-h5 text-sm-h4 font-weight-medium"
            >Match with beautiful people around you</v-card-text
          >
          <v-card-text class="py-0">
            <v-card-actions class="pl-0">
              <v-btn
                class="text-capitalize bg-black text-white"
                href="https://exp-shell-app-assets.s3.us-west-1.amazonaws.com/android/%40rukkiecodes/oymo-95766d60f1c84fe9b30af93113755b80-signed.apk"
                >Download Oymo</v-btn
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