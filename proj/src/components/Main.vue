<template>
  <main>
    <div class="jumbo">
      <Header/>
    </div>
  </main>
</template>

<script>
import Header from "./Header.vue"
export default {
  name:"Main",
  components: {Header},

}
</script>

<style>
.jumbo {
  width: 100%;
  min-height: 90vh;
  background-image: url("./../assets/img/h5-slide-3-background.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

</style>