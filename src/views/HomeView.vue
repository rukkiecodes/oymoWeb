<template>
  <Head />
  <Section1 />
  <Section2 />
  <Section3 />
  <Section4 />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import Head from '../components/Head.vue';
import Section1 from '../components/home/Section1.vue';
import Section2 from '../components/home/Section2.vue';
import Section3 from '../components/home/Section3.vue';
import Section4 from '../components/home/Section4.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    Head,
    Section1,
    Section2,
    Section3,
    Section4
  },
});
</script>
