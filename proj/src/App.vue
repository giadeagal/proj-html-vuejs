<template>
  <div id="app">
    <div class="main_wrapper">
      <Main/>
      <Footer/>
    </div>
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

.main_wrapper {
  width: 100%;
  overflow: hidden;
}
</style>