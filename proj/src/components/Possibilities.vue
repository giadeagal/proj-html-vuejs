<template>
  <section id="possibilities" class="my-5">
      <div class="container">
          <div class="row">
              <div class="col-4">
                <ul id="side-ul">
                    <li v-for="(obj, i) in sideList" :key="i" class="active text-capitalize">{{obj.text}}</li>
                </ul>
              </div>
              <div class="col-8">
                  <h2 class="px-5 pt-5">Learning possibilities</h2>
                  <p class="px-5 py-4">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatibus tenetur, pariatur deleniti quas minima ducimus cum, fugiat ex alias eaque distinctio aut porro? Fugit, asperiores dolorem autem deserunt magni perspiciatis culpa ea eaque repellendus placeat delectus tenetur, numquam omnis? Quam fuga error beatae aliquid laboriosam sit adipisci et molestiae ipsam!</p>
                  <div class="center d-flex justify-content-between">
                        <ul id="center-ul" class="">
                            <li class="pb-2"><i class="fas fa-check"></i>Lorem ipsum dolor sit amet.</li>
                            <li class="py-2"><i class="fas fa-check"></i>Lorem ipsum dolor sit amet.</li>
                            <li class="py-2"><i class="fas fa-check"></i>Lorem ipsum dolor sit amet.</li>
                        </ul>
                    <img :src="img" alt="#" class="align-self-end">
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "possibilities",
    data() {
        return {
            img: require("@/img/h12-tabs-icon-1.png"),
            sideList:[
                {
                    text:"what we do",
                    active: 1
                },
                {
                    text:"degree programme",
                    active: 0
                },
                {
                    text:"career achievements",
                    active: 0
                },
                {
                    text:"personal management",
                    active: 0
                },
                {
                    text:"steps to success",
                    active: 0
                },
                {
                    text:"knowledge transfer",
                    active: 0
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "@/styles/vars.scss";

#possibilities {
    height: 600px;
    border-bottom: 1px solid lightgray;
}

#side-ul {
    li {
        display: block;
        border: 1px solid lightgray;
        padding: 20px;
        text-transform: uppercase;
        font-weight: 500;
        font-size: 1.3rem;

        &:hover {
            border-left: 10px solid #40c4ff; 
            cursor: pointer;
            color: $myTBlue2;
            background-color: $myBGGray1;
        }
    }
}

p {
    color: $myTGray4;
    font-size: 1.3rem;
}

#center-ul {
    width: 50%;
    padding-left: 50px;

    li {
        display: block;
        text-transform: initial;
        font-size: 1.3rem;
        color: $myTGray4;

        i {
            margin-right: 15px;
            color: $myTBlue1;

            &:hover {
                cursor: initial;
            }
        }
    }
}

img {
    margin-right: 50px;
    width: 150px;
    min-height: 150px;
}
</style>