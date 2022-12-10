<template>
  <Head />
  <Section1 />
  <Section2 />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import Head from '../components/Head.vue';
import Section1 from '../components/home/Section1.vue';
import Section2 from '../components/home/Section2.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    Head,
    Section1,
    Section2
  },
});
</script>
