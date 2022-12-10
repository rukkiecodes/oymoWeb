<template>
  <Head />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import Head from '../components/Head.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    Head,
  },
});
</script>
