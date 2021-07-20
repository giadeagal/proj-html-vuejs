<template>
  <section id="empowering" class="py-5">
      <div class="container clearfix">

          <div class="float-start w-50">
              <img :src="img" alt="#" class="w-100">
          </div>

          <div class="float-start w-50">
              <h2 class="display-6 m-5 pt-5">empowering <br> children to reach their potential</h2>
            
              <p class="m-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum eaque itaque, molestiae inventore consequuntur quae mollitia, sapiente autem a non nam numquam.</p>

              <ul class="w-100">

                  <li v-for="(obj, i) in info" :key="i" class="float-start w-50 d-flex flex-column">
                      
                      <h2>{{obj.number}}</h2> 

                      <p class="in-list">{{obj.text}}</p>

                  </li>
                  
              </ul>
            </div>
      </div>
  </section>
</template>

<script>

export default {
 name: "Empowering",
 data() {
     return {
         img: require("@/img/h5-img-2.jpg"),
         info: [
             {
                 number: "168",
                 text: "user stories"
             },
             {
                 number: "347",
                 text: "events"
             }
         ]
     }
 }
}
</script>

<style scoped lang="scss">

@import "@/styles/vars.scss";

#empowering {
    height: 500px;
}

img {
    min-height: 500px;
    margin-top:150px;
}

h2 {
    text-transform: capitalize;
    font-weight: 800;
    margin-bottom:20px;
}

p:not(.in-list) {
    color: $myTGray3;
    font-size: 1.5rem;
}

li {
    color: $myTBlue1;

    h2 {
        font-size: 3rem;
    }

    p.in-list {
        font-size: 1.3rem;
        font-weight: 600;
    }
}

</style>