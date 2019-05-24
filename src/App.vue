<template>
  <div id="app">
    <Head/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Head from './components/Head.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Head,
    Footer,
  }
}
</script>

<style lang="scss">
  @import "./styles/global.scss";
</style>
