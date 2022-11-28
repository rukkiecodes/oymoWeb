<template>
  <v-app dark>
    <v-navigation-drawer
      app
      temporary
      v-model="drawer"
    >
      <v-list>
        <v-list-item
          v-for="(route, i) in routes"
          :key="i"
          :to="route.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ route.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ route.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      app
      flat
      fixed
      color="transparent"
      class="app-bar"
    >
      <v-app-bar-nav-icon
        class="hidden-sm-and-up"
        @click.stop="drawer = !drawer"
      />
      <nuxt-link
        to="/"
        class="text-decoration-none grey--text text--darken-4 text-h6"
      >{{ title }}</nuxt-link>
      <v-spacer />

      <nuxt-link
        v-for="(btn, i) in routes"
        :key="i"
        :to="btn.to"
        class="text-decoration-none grey--text text--darken-2 ml-5 hidden-xs-only"
        active-class="text--darken-4 font-weight-bold"
      >{{btn.title}}</nuxt-link>

      <v-btn
        dark
        rounded
        depressed
        class="text-capitalize ml-5"
      >Download</v-btn>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer
      app
      absolute
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data: () => ({
    drawer: false,
    title: 'Oymo',
    routes: [
      {
        to: '/about',
        icon: 'mdi-comment-question',
        title: 'Our company'
      },
      {
        to: '/faq',
        icon: 'mdi-account-question',
        title: 'FAQs'
      },
      {
        to: '/updateds',
        icon: 'mdi-update',
        title: 'Updates'
      },
      {
        to: '/contact',
        icon: 'mdi-message',
        title: 'Contact us'
      },
    ]
  })
}
</script>

<style>
* {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif !important;
}
.app-bar {
  background: rgba(255, 255, 255, 0.25);
  backdrop-filter: blur(20px);
  border-radius: 10px;
}
</style>