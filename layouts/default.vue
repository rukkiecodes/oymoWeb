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
          to="/product"
        >
          <v-list-item-content>
            <v-list-item-title>Product</v-list-item-title>
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
      class="appBar"
    >
      <v-app-bar-nav-icon
        @click="drwer = !drwer"
        class="hidden-sm-and-up"
      />
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
    <v-footer
      class="mt-12"
      color="transparent"
    >
      <v-container>
        <v-row
          justify="start"
          align="start"
        >
          <v-col cols="12">
            <span class="text-uppercase black--text font-weight-bold mr-5">
              GET THE APP!
            </span>
            <v-btn
              dark
              large
              rounded
              color="black"
              class="text-capitalize"
              href="https://exp-shell-app-assets.s3.us-west-1.amazonaws.com/android/%40rukkiecodes/oymo-23d92dc94cac4bd7a2a38ae2ba25208e-signed.apk"
            >
              Download
            </v-btn>
          </v-col>
          <v-col
            cols="12"
            sm="4"
          >
            <p class="text-h6 font-weight-bold text-uppercase">Legal</p>

            <p
              v-for="(legal, i) in legals"
              :key="i"
              class="text-body-2 mt-n2"
            >
              <nuxt-link :to="legal.to" class="text-decoration-none grey--text text--darken-3">
                {{legal.title}}
              </nuxt-link>
            </p>
          </v-col>
          <v-col
            cols="12"
            sm="4"
          >
            <p class="text-h6 font-weight-bold text-uppercase">SOCIAL</p>

            <div class="d-fles">
              <v-btn
                fab
                small
                depressed
                class="mr-5"
                href="https://www.facebook.com/oymoDates"
              >
                <v-icon>mdi-facebook</v-icon>
              </v-btn>
              <v-btn
                fab
                small
                depressed
                class="mr-5"
                href="https://twitter.com/rukkiecodes"
              >
                <v-icon>mdi-twitter</v-icon>
              </v-btn>
            </div>
          </v-col>
          <v-col
            cols="12"
            sm="4"
          >
            <p class="text-h6 font-weight-bold text-uppercase">Feedback</p>
            <v-text-field
              solo
              dense
              class="rounded-lg"
              placeholder="Email"
            />
            <v-textarea
              solo
              dense
              rows="3"
              no-resize
              class="rounded-lg"
              placeholder="Feedback"
            />
            <v-btn
              color="red darken-1"
              class="rounded-lg"
              depressed
              rounded
              block
              dark
            >
              Send
            </v-btn>
          </v-col>
        </v-row>
        <v-divider class="my-5" />
        <span class="text-caption grey--text text--darken-3">
          ©Oymo {{ new Date().getFullYear() }}, All Rights Reserved
        </span>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data: () => ({
    drwer: false,
    legals: [
      { title: 'Privacy policy', to: '/policy' },
      { title: 'Terms of Use', to: '/terms' }
    ]
  })
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
  background: rgba(244, 247, 248, 0.26) !important;
  backdrop-filter: blur(4px);
}
</style>