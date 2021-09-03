<template>
  <v-app>
  <v-main>
    <panel></panel>
    <router-view></router-view>
    <Footer/>
  </v-main>
  </v-app>
</template>

<script>
import panel from './components/panel.vue';
import Footer from './components/footer'
export default {
  components: { panel,Footer },



  data: () => ({
    //
  }),
};
</script>
<style>
  *{
    scroll-behavior: smooth;

  }
</style>
