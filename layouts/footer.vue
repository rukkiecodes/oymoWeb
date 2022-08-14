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
          <div class="d-flex">
            <v-text-field
              solo
              dense
              class="rounded-lg mr-1"
              placeholder="Your name"
              v-model="credential.name"
            />
            <v-text-field
              solo
              dense
              placeholder="Email"
              class="rounded-lg ml-1"
              v-model="credential.email"
            />
          </div>
          <v-textarea
            solo
            dense
            rows="3"
            no-resize
            class="rounded-lg"
            placeholder="Feedback"
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
      <span class="text-caption grey--text text--darken-3">
        ©Oymo {{ new Date().getFullYear() }}, All Rights Reserved
      </span>
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
      { title: 'Terms of Use', to: '/terms' }
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
