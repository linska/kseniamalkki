<template>
  <v-app>

    <NavBar/>

    <Hero/>

  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld';
import NavBar from './components/NavBar';
import Hero from './components/Hero';

export default {
  name: 'App',

  components: {
    NavBar,
    Hero,
  },

  data: () => ({
    //
  }),
};
</script>
