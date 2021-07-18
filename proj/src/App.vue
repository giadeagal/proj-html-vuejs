<template>
  <div id="app">
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Main from"./components/Main.vue"
import Footer from"./components/Footer.vue"


export default {
  name: 'App',
  components: {
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import "@/styles/commons.scss";
</style>