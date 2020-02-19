<template>
  <v-app>
    <Bar/>
      <HelloWorld/>
  </v-app>
</template>

<script>
import Bar from '@/components/Bar';
import HelloWorld from '@/components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld, Bar
  },

  data: () => ({
    //
  }),
};
</script>
