<template>
  <div
    fluid
    class="pa-0 ma-0 pt-5 head"
  >
    <v-container>
      <v-row
        justify="space-between"
        align="center"
      >
        <v-col
          cols="12"
          sm="6"
          md="6"
        >
          <span class="text-h4 text-sm-h3 font-weight-bold grey--text text--darken-3">
            Find friends, and dates around you with just a swipe.
          </span>
          <br />
          <v-btn
            dark
            large
            rounded
            color="black"
            class="mt-5 text-capitalize"
            href="https://exp-shell-app-assets.s3.us-west-1.amazonaws.com/android/%40rukkiecodes/oymo-23d92dc94cac4bd7a2a38ae2ba25208e-signed.apk"
          >
            Download
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<style lang="scss" scoped>
.head {
  background-image: url("../../assets/bg.png");
  background-size: cover;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  height: 100vh;
  display: flex;
  align-items: center;
}
</style>