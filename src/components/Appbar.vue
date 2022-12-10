<template>
  <v-navigation-drawer app temporary v-model="drawer">
    <v-list lines="one" nav>
      <v-list-item
        v-for="(route, i) in routes"
        :key="i"
        :title="route.title"
        :prepend-icon="route.icon"
        :to="route.to"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
  <v-app-bar app flat color="transparent" class="app-bar">
    <v-app-bar-nav-icon
      class="hidden-sm-and-up"
      @click.stop="drawer = !drawer"
    />
    <router-link
      to="/"
      class="text-decoration-none text-grey-darken-4 text-h6 ml-5"
      >{{ title }}</router-link
    >
    <v-spacer />

    <router-link
      v-for="(btn, i) in routes"
      :key="i"
      :to="btn.to"
      class="text-decoration-none text-grey-darken-2 ml-5 d-none d-sm-flex"
      active-class="text-grey-darken-4 font-weight-bold"
      >{{ btn.title }}</router-link
    >

    <v-btn
      color="black"
      class="text-capitalize ml-5"
      href="https://exp-shell-app-assets.s3.us-west-1.amazonaws.com/android/%40rukkiecodes/oymo-95766d60f1c84fe9b30af93113755b80-signed.apk"
      >Download</v-btn
    >
  </v-app-bar>
</template>

<script>
export default {
  name: "DefaultLayout",
  data: () => ({
    drawer: false,
    title: "Oymo",
    routes: [
      {
        to: "/about",
        icon: "mdi-comment-question",
        title: "Our company",
      },
      {
        to: "/faq",
        icon: "mdi-account-question",
        title: "FAQs",
      },
      {
        to: "/updateds",
        icon: "mdi-update",
        title: "Updates",
      },
      {
        to: "/contact",
        icon: "mdi-message",
        title: "Contact us",
      },
    ],
  }),
};
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