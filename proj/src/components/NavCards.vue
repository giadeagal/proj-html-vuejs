<template>
  <section>
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-2 text-center" v-for="(obj, i) in cards" :key="i">
                  <div class="card">
                      <img :src="obj.img" alt="obj.text">
                      <p>{{obj.text}}</p>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name:"NavCards",
    data() {
        return {
            cards: [
                {
                    text:"languages",
                    img:require("@/img/h5-custom-icon-1.png")
                },
                {
                    text:"software",
                    img:require("@/img/h5-custom-icon-2.png")
                },
                {
                    text:"business",
                    img:require("@/img/h5-custom-icon-3.png")
                },
                {
                    text:"chemistry",
                    img:require("@/img/h5-custom-icon-4.png")
                },
                {
                    text:"science",
                    img:require("@/img/h5-custom-icon-5.png")
                },
                {
                    text:"DIY & craft",
                    img:require("@/img/h5-custom-icon-6.png")
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

@import "@/styles/vars.scss";

    section {
        padding: 50px 0;
    }

    .card {
        min-height: 250px;
        border: none;
        background-color: $myBGBlue2;

        &:hover {
            cursor: pointer;
        }

        img {
            width: 80px;
            min-height: 80px;
            margin:auto;
        }

        &:hover img {
            position: relative;
            bottom: 20px;
        }

        p {
            font-weight: 800;
            text-transform: capitalize;
        }
    }
</style>