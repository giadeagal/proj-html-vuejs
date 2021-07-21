<template>
  <section>
      <p id="number">{{details.number}}</p>
      <p id="text">{{details.text}}</p>
  </section>
</template>

<script>
export default {
    name:"Counter",
    props: {
        details: Array
    }
}
</script>

<style scoped lang="scss">

@import "@/styles/vars.scss";

</style>