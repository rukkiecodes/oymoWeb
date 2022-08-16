<template>
  <v-container>
    <v-slide-group
      v-model="model"
      v-if="feedbacks.length >= 10"
      class="pa-4 px-0 mx-0"
    >
      <v-slide-item
        v-for="(feedback, i) in feedbacks"
        :key="i"
      >
        <v-card
          class="ma-2"
          min-height="100"
          max-height="300"
          width="250"
          flat
          outlined
        >
          <v-card-title>
            {{feedback.name}}
          </v-card-title>
          <v-card-text>
            {{feedback.feedback}}
          </v-card-text>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    model: null,
    feedbacks: []
  }),

  mounted () {
    this.$nextTick(async () => {
      const result = await this.$axios({
        method: 'get',
        url: 'https://oymo.herokuapp.com/get'
      })
      this.feedbacks = []
      this.feedbacks.push(...result.data.feedbacks)
    })
  }
}
</script>