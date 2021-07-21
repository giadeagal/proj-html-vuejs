<template>
  <footer>
    <div class="container">
      <section id="f-top">
        <div class="row">
          <div class="col-3 gray">
            <img :src="logo" alt="">
            <p class="gray text-capitalize py-5">providing life changing experiences through education. class that fit your busy life. closer to home</p>
            <p class="pb-3">
              <i class="fas fa-phone-alt clear"></i>
              <span>1-677-124-44227</span>
            </p> 
            <p>
              <i class="far fa-clock clear"></i>
              <span>mon - sat 8.00 - 18.00</span>
            </p> 
          </div>
          <div class="col-3 gray">
            <h2 class="pt-5">popular courses</h2>
            <ul v-for="(obj, i) in staff" :key="i">
              <li class="important">{{obj.position}}</li>
              <li>{{obj.fullName}}</li>
            </ul>
          </div>
          <div class="col-3 gray">
            <h2 class="pt-5">support</h2>
            <ul>
              <li v-for="(str, i) in support" :key="i+a" class="mb-4 support">
                {{support[i]}}
              </li>
            </ul>
          </div>
          <div class="col gray">
            <h2 class="pt-5">flexible learning</h2>
            <img :src="img" alt="map" id="map">
          </div>
        </div>
      </section>
      <section id="f-bottom" class="d-flex justify-content-between py-5">
        <div class="left text-nowrap"><p>Copyryghts 2017 &copy;mikado themes</p></div>
        <div class="right">
          <p class="text-nowrap text-uppercase"> call +44 300 303 0266 
            <span class="px-3">follow us 
              <i class="fab fa-twitter clear"></i>
              <i class="fab fa-instagram clear"></i>
              <i class="fab fa-facebook-f clear"></i>
            </span>
          </p>
        </div>
      </section>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      logo: require("@/img/logo-light.png"),
      img: require("@/img/footer-img-1.png"),
      staff: [
        {
          position:"business english",
          fullName: "preston marshall"
        },
        {
          position:"social computing",
          fullName: "david sanders"
        },
        {
          position:"learn spanish",
          fullName: "jennie king"
        }
      ],
      support: ["user dashboard", "contact us", "FAQ", "course offer", "events" ]
    }
  }
}
</script>

<style lang="scss">
@import "@/styles/vars.scss";
footer {
  background-color: $myBGBlack;

  .gray {
    color: gray
  }

  #f-top {
    border-bottom: 1px solid lightgray;
    padding: 100px 0;
  }
  
  h2 {
    color: white;
  }

  p {
    width: 80%;

    i {
      margin-right: 10px;

      &:hover {
      color: $myTBlue2;
      }

    }
    
    span {
      color: $myTGray1;
      text-transform: capitalize;

    }
  }

  ul {
    li {
      text-transform: capitalize;
      font-size: 1.2rem;
      margin-left: -35px;
      display: block;
    }

    li.important {
      color: $myTGray1;
      
      &:hover {
        color: $myTBlue2;
        cursor: pointer;
      }
    }

  }

  #map {
    width: 80%;
    min-height: 150px;
  }
}


.support:hover {
        color: $myTBlue2;
        cursor: pointer;
      }


#f-bottom {
  p {
    color: gray;
    span {
      color: gray;
      text-transform: uppercase;

      i {
        margin-left: 20px;
      }
    }
  }
  .left {
    
    text-transform: capitalize;
  }
}
</style>