<template>
  <secion id="trusted-name">
      
      <div class="container">
          <h2 class="display-6">the trusted name <br> for in - home tutoring</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum eaque itaque, molestiae inventore consequuntur quae mollitia, sapiente autem a non nam numquam. Reprehenderit iusto aut, omnis ea doloribus ex neque quidem minus corporis beatae odit alias dolorum at temporibus ullam, eligendi dolore in nostrum illum ipsam! Id error harum eaque.   </p>
          <a href="#">learn more</a>
          <img :src="img" alt="">
          <Elevator/>
      </div>
      
  </secion>
</template>

<script>
import Elevator from "./Elevator.vue"

export default {
    name: "TrustedName",
    components: {
        Elevator
    },
    data() {
        return {
            img:require('@/img/h5-img-1.jpg')
        }
    }
}
</script>

<style lang="scss" scoped>

@import "@/styles/vars.scss";

#elevator {
    position: absolute;
    top: 2000px;
    right:0;
}

h2 {
    text-transform: capitalize;
    font-weight: 800;
    margin-top: 80px;
    margin-bottom:20px;
}

p {
    color: $myTGray3;
    font-size: 1.5rem;
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