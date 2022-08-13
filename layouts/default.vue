<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drwer"
      absolute
      temporary
      app
    >
      <v-list dense>
        <v-list-item link to="/">
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link to="/product">
          <v-list-item-content>
            <v-list-item-title>Product</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link to="/learn">
          <v-list-item-content>
            <v-list-item-title>Learn</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link to="/safety">
          <v-list-item-content>
            <v-list-item-title>Safety</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      fixed
      flat
      class="appBar"
    >
      <v-app-bar-nav-icon @click="drwer = !drwer" class="hidden-sm-and-up" />
      <v-toolbar-title class="logo text-h4 mb-2">
        Oymo
      </v-toolbar-title>
      <v-btn
        depressed
        rounded
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/"
      >
        Home
      </v-btn>
      <v-btn
        depressed
        rounded
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/product"
      >
        Product
      </v-btn>
      <v-btn
        depressed
        rounded
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/learn"
      >
        Learn
      </v-btn>
      <v-btn
        depressed
        rounded
        color="transparent"
        active-class="red darken-1 white--text"
        class="text-capitalize ml-4 hidden-xs-only"
        to="/safety"
      >
        Safety
      </v-btn>
      <v-spacer />
      <v-btn
        color="black"
        class="text-capitalize"
        rounded
        dark
      >
        Download
      </v-btn>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data: () => ({
    drwer: false
  })
}
</script>


<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");

.logo {
  font-family: "Pacifico", cursive !important;
  line-height: 60px;
}

.appBar {
  background: rgba(244, 247, 248, 0.26) !important;
  backdrop-filter: blur(4px);
}
</style>