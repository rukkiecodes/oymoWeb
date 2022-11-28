<template>
  <v-container>
    <section1Vue />
    <section2Vue />
  </v-container>
</template>

<script>
import section1Vue from '~/components/index/section1.vue';
import section2Vue from '~/components/index/section2.vue';
export default {
  name: 'IndexPage',

  components: {
    section1Vue,
    section2Vue
  }
}
</script>
