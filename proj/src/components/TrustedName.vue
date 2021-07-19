<template>
  <secion id="trusted-name">
      <div class="container">
          <h2 class="display-6">the trusted name <br> for in - home tutoring</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum eaque itaque, molestiae inventore consequuntur quae mollitia, sapiente autem a non nam numquam. Reprehenderit iusto aut, omnis ea doloribus ex neque quidem minus corporis beatae odit alias dolorum at temporibus ullam, eligendi dolore in nostrum illum ipsam! Id error harum eaque.   </p>
          <a href="#">learn more</a>
          <img :src="img" alt="">
      </div>
  </secion>
</template>

<script>
export default {
    name: "TrustedName",
    data() {
        return {
            img:require('@/img/h5-img-1.jpg')
        }
    }
}
</script>

<style lang="scss" scoped>

@import "@/styles/vars.scss";

h2 {
    text-transform: capitalize;
    font-weight: 800;
    margin-top: 80px;
    margin-bottom:20px;
}

p {
    color: $myTGray3;
}

a {
    color: $myTBlue1;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: 800;
}

img {
    width: 100%;
    min-height: 800px;
}

</style>