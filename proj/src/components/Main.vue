<template>
  <main>
    <div class="jumbo">
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

    <!-- Sezione NavCards -->
    <NavCards/>
    <!-- /sezione NavCards -->
  </main>
</template>

<script>
import Header from "./Header.vue"
import NavCards from "./NavCards.vue"
export default {
  name:"Main",
  components: {
    Header,
    NavCards
    }

}
</script>


<style lang="scss">
@import "@/styles/vars.scss";

.jumbo {
  width: 100%;
  height: 90vh;
  background-image: url("./../assets/img/h5-slide-3-background.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  color: white;
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

  &:not(.active) {
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

</style>