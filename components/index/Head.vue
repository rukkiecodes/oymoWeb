<template>
  <div
    fluid
    class="pa-0 ma-0 pt-5 head"
  >
    <v-container>
      <v-row justify="space-between" align="center">
        <v-col cols="12" sm="6" md="6">
          <span class="text-h4 text-sm-h3 font-weight-bold grey--text text--darken-3">
            Find friends, and dates around you with just a swipe.
          </span>
          <br />
          <v-btn color="black" class="mt-5 text-capitalize" large rounded dark>
            Download
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {

}
</script>

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