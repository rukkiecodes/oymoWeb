<template>
  <v-container
    fluid
    class="ma-0 pa-0"
  >
    <Head />
    <About />
  </v-container>
</template>

<script>
import Head from '~/components/about/Head.vue'
import About from '~/components/about/About.vue';
export default {
  name: "IndexPage",
  components: { Head, About }
}
</script>
