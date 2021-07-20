<template>
  <aside>
      <a href="#" v-for="(img, i) in imgs" :key="i">
          <img :src="imgs[i]" alt="">
      </a>
  </aside>
</template>

<script>
export default {
    name: "SideButtons",
    data() {
        return {
            imgs: [require("@/img/svg/svg-3.svg"), require("@/img/svg/svg-2.svg")]
        }
    }
}
</script>
