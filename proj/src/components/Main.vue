<template>
  <main>
    <div class="jumbo" id="elevate-here">
      <Header/>
      <div class="flexer">
        <div class="center_group">
          <h2 class="display-1">contemporary ideas</h2>
          <p class="py-5">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Debitis tempora qui a minus nisi quae vero quas illum quod culpa?</p>
          <div class="my_btn">
            <a href=""><strong>register now</strong></a>
          </div>
        </div>
        <div class="bottom_group">
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle fa-xs active"></i>
        </div>
      </div>
    </div>

    <!-- Bottoni laterali -->
    <Elevator/>
    <AsideButtons/>
    <!-- Fine bottoni laterali -->

    <!-- elenco sezioni top-->
    <NavCards/>
    <TrustedName/>
    <Empowering/>
    <!-- Fine elenco sezioni top -->

    <!-- Jumbo2 -->
    <div class="jumbo" id="jumbo2">
      <div class="flexer">
        <div class="center_group">
          <img :src="img" alt="">
          <p class="py-5">"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facere quibusdam dolorum quisquam, aut non odio dolores placeat vero fugiat error blanditiis voluptas similique saepe velit exercitationem minus. Voluptatibus deserunt temporibus iste consectetur explicabo odit quae dolore at adipisci ipsa eius voluptatum quisquam unde quam recusandae earum totam quasi, harum minus culpa quidem quos. Atque cumque veritatis modi doloribus non nostrum quaerat enim autem doloremque natus vitae, ducimus blanditiis perferendis labore dignissimos eligendi velit accusantium. Rerum, suscipit? Id perferendis doloribus impedit."</p>
          <div id="reviewer">
            <h2 class="my-3">joan collins</h2>
            <h4>student</h4>
          </div>
        </div>
        <div class="bottom_group">
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle fa-xs active"></i>
          <i class="fas fa-circle"></i>
        </div>
      </div>
    </div>
    <!-- Fine Jumbo 2 -->

    <!-- elenco sezioni bottom -->
    <Possibilities/>
    <!-- fine elenco sezioni bottom -->


  </main>
</template>

<script>
import Header from "./Header.vue"
import NavCards from "./NavCards.vue"
import TrustedName from "./TrustedName.vue"
import Empowering from "./Empowering.vue"
import Possibilities from "./Possibilities"
import Elevator from "./Elevator.vue"
import AsideButtons from "./AsideButtons.vue"
export default {
  name:"Main",
  components: {
    Header,
    NavCards,
    TrustedName,
    Empowering,
    Possibilities,
    Elevator,
    AsideButtons
    },
  data() {
    return {
      img: require("@/img/testimonials-standard-2.png")
    }
  }
}
</script>


<style lang="scss">
@import "@/styles/vars.scss";

.jumbo {
  width: 100%;
  height: 90vh;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  color: white;
}

#elevate-here {
    background-image: url("./../assets/img/h5-slide-3-background.jpg");
}

#jumbo2 {
    background-image: url("./../img/h5-parallax-img-1.png");

    img {
      width: 200px;
      min-height: 200px;
    }

    p {
      font-size: 1.3rem;
    }

    #reviewer {

      h2 {
        text-transform: capitalize;
      }

      h4 {
        text-transform: uppercase;
      }

    }
}


.flexer {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: calc(90vh - 100px);
  width: 100%;
  text-align: center;

}

h2 {
  text-transform: capitalize;
}

.my_btn {
  height: 45px;
  width: 200px;  
  margin: auto;

  a {
    background-color: $myBGBlue3;
    height: 100%;
    width: 100%;
    padding: 20px;
    text-decoration: none;
    color: white;
    text-transform: uppercase;

    &:hover {
      background-color: $myBGBlue4;
      text-decoration: none;
      color: white;
    }
  }

.bottom_group {
  height: 20px;
  width: 100%;
}
  
}

i {
  margin: 0 5px;

  &:not(.active, .clear) {
  opacity:0.5;
}

  &.active {
    border: 1px solid white;
    border-radius: 50%;
    padding: 2px;
  }

  &:hover {
    cursor:pointer;
    opacity: 1;
  }
}

#elevator {
        background-color: $myBGBlue4;
        color: white;
        position: fixed;
        bottom:0;
        right: 20px;
        width: 70px;
        height: 70px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-decoration: none;

        p {
            text-transform: uppercase;
            font-weight: 600;
        }
    }

aside {
    position: fixed;
    right: 15px;
    top: 60%;
    width: 30px;
}
</style>