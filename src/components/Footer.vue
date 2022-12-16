<template>
  <v-divider />
  <v-container>
    <v-footer color="white">
      <v-row justify="space-between" align="start">
        <v-col cols="12" class="text-center">
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            :icon="icon.name"
            color="#FF4040"
            variant="text"
          />
        </v-col>

        <v-col
          cols="12"
          sm="6"
          class="
            d-flex
            flex-row flex-sm-column flex-wrap
            pl-0
            justify-start
            align-start
          "
        >
          <router-link
            v-for="(btn, i) in routes"
            :key="i"
            :to="btn.to"
            class="
              text-decoration-none text-grey-darken-2
              ml-5
              font-weight-medium
            "
            active-class="text-grey-darken-4 font-weight-bold"
            >{{ btn.title }}</router-link
          >
        </v-col>

        <v-col cols="12" sm="6">
          <ContactFormVue />
        </v-col>
        <v-col cols="12" class="text-center">
          <span class="text-grey--darken-4"
            >{{ new Date().getFullYear() }} — <strong>Oymo</strong></span
          >
        </v-col>
      </v-row>
    </v-footer>
  </v-container>
</template>

<script>
import ContactFormVue from "./fragments/ContactForm.vue";
export default {
  components: {
    ContactFormVue,
  },
  data: () => ({
    icons: [
      { name: "mdi-facebook" },
      { name: "mdi-twitter" },
      { name: "mdi-linkedin" },
      { name: "mdi-instagram" },
    ],
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