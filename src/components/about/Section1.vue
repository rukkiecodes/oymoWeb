<template>
  <v-row class="mt-12" justify="space-between">
    <v-col cols="12" sm="6" order="1" order-sm="0">
      <v-card flat>
        <v-card-text class="pa-0">
          <span
            class="
              bg-red-lighten-5
              text-red
              font-weight-medium
              px-4
              py-2
              rounded-lg
              text-uppercase
            "
            >Our Vission</span
          >
          <br />
          <br />
          Find friends, and dates around you with just a swipe. Oymo is a
          communication platform, which offers a comfortable and safe
          environment for men and women to find the love of their life. Find
          friends, and dates around you with just a swipe. Are you bored? Enjoy
          the wide collection of interesting shorts. Like, comment, interact
          with users, and find love❤️ around you.
        </v-card-text>
        <v-card-text class="pa-0 mt-16">
          <span
            class="
              bg-red-lighten-5
              text-red
              font-weight-medium
              px-4
              py-2
              rounded-lg
              text-uppercase
            "
            >What are we</span
          >
          <br />
          <br />
          As you may know, they are a lot of dating apps and meetup apps. That
          is expensive and not engaging enough to keep users entertained.😥 This
          is where Oymo comes in. Oymo is a cheap-to-use communication platform,
          easy to use, keeps users entertained, and allows users to meet
          beautiful people around their neighborhood and around the world
          🌍💃💃🏻💃🏽
        </v-card-text>
      </v-card>
    </v-col>
    <v-col cols="12" sm="5" class="d-flex justify-center">
      <v-carousel
        cycle
        hide-delimiter-background
        hide-delimiters
        :show-arrows="false"
        height="500"
      >
        <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="slide" />
      </v-carousel>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    slides: [
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1671222901/hero_bi5x5k.png",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1671222896/reels_h5bgl2.png",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1671222895/chat_o8oiyk.png",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1671222894/match_az85ob.png",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1663778406/omm_xntrx5.jpg",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1663779674/WhatsApp_Image_2022-08-09_at_1.53.28_AM_1_pzdlky.jpg",
      "https://res.cloudinary.com/rukkiecodes/image/upload/v1663779675/om2_k8rzve.jpg",
    ],
  }),
};
</script>
