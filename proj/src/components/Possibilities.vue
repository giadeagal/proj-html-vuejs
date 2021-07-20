<template>
  <section id="possibilities" class="my-5">
      <div class="container">
          <div class="row">
              <div class="col-4">
                <ul id="side-ul">
                    <li v-for="(obj, i) in sideList" :key="i" class="active text-capitalize">{{obj.text}}</li>
                </ul>
              </div>
              <div class="col"></div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "possibilities",
    data() {
        return {
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
    height: 800px;
    border-bottom: 1px solid lightgray;
}

#side-ul {
    li {
        display: block;
        border: 1px solid lightgray;
        padding: 20px;
        text-transform: uppercase;
        font-weight: 500;

        &:hover {
            border-left: 10px solid #40c4ff; 
            cursor: pointer;
            color: $myTBlue1;
            background-color: $myBGGray1;
        }
    }
}
</style>