<template>
  <v-container
    fluid
    class="ma-0 pa-0"
  >

    <Head />
    <About />
    <Testimonials />
  </v-container>
</template>

<script>
import Head from '~/components/index/Head.vue';
import About from '~/components/index/About.vue';
import Testimonials from '~/components/index/Testimonials.vue';
export default {
  name: "IndexPage",
  components: { Head, About, Testimonials }
}
</script>
