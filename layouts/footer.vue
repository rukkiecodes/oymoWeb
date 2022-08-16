<template>
  <v-footer
    class="mt-12"
    color="transparent"
  >
    <v-container>
      <v-row
        justify="start"
        align="start"
      >
        <v-col
          cols="12"
          sm="3"
        >
          <p class="text-h6 font-weight-bold text-uppercase">DOCUMENTS</p>

          <p
            v-for="(legal, i) in legals"
            :key="i"
            class="text-body-2 mt-n2"
          >
            <nuxt-link
              :to="legal.to"
              class="text-decoration-none grey--text text--darken-3"
            >
              {{legal.title}}
            </nuxt-link>
          </p>
        </v-col>
        <v-col
          cols="12"
          sm="3"
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
          sm="6"
        >
          <p class="text-h6 font-weight-bold text-uppercase">Feedback</p>
          <div class="d-flex">
            <v-text-field
              dense
              class="mr-1"
              color="grey darken-3"
              label="Your name"
              v-model="credential.name"
            />
            <v-text-field
              dense
              class="ml-1"
              label="Email"
              color="grey darken-3"
              v-model="credential.email"
            />
          </div>
          <v-textarea
            dense
            rows="2"
            no-resize
            color="grey darken-3"
            label="Feedback"
            v-model="credential.feedback"
          />
          <v-btn
            dark
            block
            rounded
            depressed
            class="rounded-lg"
            color="red darken-1"
            @click="sendFeedback"
            :loading="loading"
          >
            Send
          </v-btn>
        </v-col>
      </v-row>
      <v-divider class="my-5" />
      <v-row
        justify="space-between"
        align="center"
      >
        <div class="d-flex">
          <nuxt-link
            v-for="(legal, i) in legals"
            :key="i"
            :to="legal.to"
            class="text-caption grey--text text--darken-3 mr-2"
          >
            {{ legal.title }}
          </nuxt-link>
        </div>
        <span class="text-caption grey--text text--darken-3">
          ©Oymo {{ new Date().getFullYear() }}, All Rights Reserved
        </span>
      </v-row>
    </v-container>

    <v-snackbar
      v-model="snackbar"
      color="white"
      left
      bottom
    >
      <span class="grey--text text--darken-4 font-weight-bold">{{ text }}</span>
    </v-snackbar>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    loading: false,
    snackbar: false,
    text: '',
    legals: [
      { title: 'Privacy policy', to: '/policy' },
      { title: 'Terms of Use', to: '/terms' },
      { title: 'About Oymo', to: '/about' },
      { title: 'Safety', to: '/safety' }
    ],
    credential: {
      name: '',
      email: '',
      feedback: ''
    }
  }),

  methods: {
    sendFeedback () {
      this.loading = true
      this.$axios({
        method: 'post',
        url: 'https://oymo.herokuapp.com',
        data: {
          name: this.credential.name,
          email: this.credential.email,
          feedback: this.credential.feedback
        }
      }).then(result => {
        this.loading = false
        this.snackbar = true
        this.text = result.data.message
        this.credential.name = ''
        this.credential.email = ''
        this.credential.feedback = ''
      }).catch(error => {
        console.log(error)
        this.loading = false
      })
    }
  }
}
</script>
