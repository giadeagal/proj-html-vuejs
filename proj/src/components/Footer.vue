<template>
  <footer>
    <div class="container">
      <section id="f-top">
        <div class="row">
          <div class="col-3 gray">
            <img :src="logo" alt="">
            <p class="gray text-capitalize py-5">providing life changing experiences through education. class that fit your busy life. closer to home</p>
            <p>
              <i class="fas fa-phone-alt clear"></i>
            </p> 
          </div>
          <div class="col-3 gray">
            <h2 class="pt-5">popular courses</h2>
          </div>
          <div class="col-3 gray">
            <h2 class="pt-5">support</h2>
          </div>
          <div class="col gray">
            <h2 class="pt-5">flexible learning</h2>
            <img :src="img" alt="map" id="map">
          </div>
        </div>
      </section>
      <section id="f-bottom"></section>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      logo: require("@/img/logo-light.png"),
      img: require("@/img/footer-img-1.png")
    }
  }
}
</script>

<style lang="scss">
@import "@/styles/vars.scss";
footer {
  height: 900px;
  background-color: $myBGBlack;

  .gray {
    color: gray
  }

  #f-top {
    border-bottom: 10px solid lightgray;
    padding: 100px 0;
  }
  
  h2 {
    color: white;
  }

  p {
    width: 80%;
  }

  #map {
    width: 80%;
    min-height: 150px;
  }
}


</style>