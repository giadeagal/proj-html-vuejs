<template>
  <section id="popular">
      <div class="container">

            <h2 class="text-center text-capitalize display-4">popular online courses</h2>

            <p class="text-center pt-3 pb-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum vero corrupti sint. Earum cupiditate incidunt ducimus, nulla iusto perspiciatis tempora, optio numquam mollitia eum velit error corporis, similique hic consequuntur dolor excepturi fugiat aut maxime sint. Doloremque voluptate eum impedit.</p>

            <div class="row">
                <div class="col-4" v-for="(obj, i) in courses" :key="i">
                    <img :src="obj.img" alt="obj.alt">
                </div>
            </div>
      </div>
  </section>
</template>

<script>
export default {
    name:"Popular",
    data() {
        return {
            courses: [
            {
                img: require("@/img/landing-carousel-gallery-img-3.jpg"),
                alt:"leaders-1"
            },
            {
                img:require("@/img/landing-carousel-gallery-img-5.jpg"),
                alt:"leaders-2"
            },
            {
                img:require("@/img/landing-carousel-gallery-img-1.jpg"),
                alt:"Business English"
            }
        ]
        }
    }

}
</script>

<style scoped lang="scss">

#popular {
    height: 900px;
    border-bottom: 1px solid lightgray;
    background-image: url("./../img/page-background-img.png");

    img {
        width: 100%;
        min-height: 550px;
    }
}

</style>