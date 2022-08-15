<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drwer"
      absolute
      temporary
      app
    >
      <v-list dense>
        <v-list-item
          link
          to="/"
        >
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link
          to="/about"
        >
          <v-list-item-content>
            <v-list-item-title>About</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link
          to="/learn"
        >
          <v-list-item-content>
            <v-list-item-title>Learn</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link
          to="/safety"
        >
          <v-list-item-content>
            <v-list-item-title>Safety</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      flat
      color="white"
    >
      <v-app-bar-nav-icon
        @click="drwer = !drwer"
        class="hidden-sm-and-up"
      />
      <v-toolbar-title class="logo text-h4 mb-2 black--text">
        Oymo
      </v-toolbar-title>
      <v-btn
        rounded
        depressed
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/"
      >
        Home
      </v-btn>
      <v-btn
        rounded
        depressed
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/about"
      >
        About
      </v-btn>
      <v-btn
        rounded
        depressed
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/learn"
      >
        Learn
      </v-btn>
      <v-btn
        rounded
        depressed
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/safety"
      >
        Safety
      </v-btn>
      <v-spacer />
      <v-btn
        dark
        rounded
        color="black"
        class="text-capitalize"
        href="https://exp-shell-app-assets.s3.us-west-1.amazonaws.com/android/%40rukkiecodes/oymo-23d92dc94cac4bd7a2a38ae2ba25208e-signed.apk"
      >
        Download
      </v-btn>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./footer.vue";
export default {
    name: "DefaultLayout",
    data: () => ({
        drwer: false
    }),
    components: { Footer }
}
</script>


<style lang="scss" scoped>
@font-face {
  font-family: Pacifico;
  src: url("../assets/Pacifico/Pacifico-Regular.ttf") format("truetype");
}

.logo {
  font-family: Pacifico !important;
  line-height: 60px;
}

.appBar {
  background: rgba(0, 0, 0, 0.26) !important;
  backdrop-filter: blur(10px);
}
</style>