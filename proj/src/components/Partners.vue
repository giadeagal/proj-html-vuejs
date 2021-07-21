<template>
  <section id="partners">
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-3" v-for="(obj, i) in logos" :key="i">
                  <img :src="obj.img" :alt="obj.alt">
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name:"Partners",
    data() {
        return {
            logos: [
                {
                    img:require("@/img/h5-client-5.png"),
                    alt:"iAcademy"
                },
                {
                    img:require("@/img/h5-client-1.png"),
                    alt:"Study Central"
                },
                {
                    img:require("@/img/h5-client-2.png"),
                    alt:"Educator"
                },
                {
                    img:require("@/img/h5-client-3.png"),
                    alt:"Belgrade university"
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">


    #partners {
        margin: 100px 0;

        img {
            max-width: 100%;
            min-height: 60px;
        }
    }
</style>