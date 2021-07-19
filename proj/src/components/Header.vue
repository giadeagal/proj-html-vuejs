<template>
  <header>
    
      <nav>
      <div class="container">
        <a href="#" class="float-start">
          <div class="logo">
            <img :src="require('@/assets/img/logo-light.png')" alt="logo">
            <div class="underline"></div>
          </div>
        </a>
        <ul class="float-end">
          <li v-for="(obj, i) in navItems" :key="i" class="mx-3">
            <a :href="obj.link">{{obj.text}}</a>
          </li>
          <li class="mx-3">
            <a href="#"><i class="fas fa-search clear"></i></a>
          </li>
          <li class="mx-3">
            <a href="#"><i class="fas fa-shopping-bag clear"></i></a>
          </li>
          <li class="mx-3">
            <a href="#"><i class="fas fa-bars clear"></i></a>
          </li>
        </ul>
        </div>
    </nav>
    
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      navItems: [
        {
          text: "home",
          link: "#"
        },
        {
          text: "courses",
          link: "#"
        },
        {
          text: "instructors",
          link: "#"
        },
        {
          text: "events",
          link: "#"
        },
        {
          text: "pages",
          link: "#"
        },
        {
          text: "elements",
          link: "#"
        }
      ]
    }
  }
}
</script>

<style lang="scss">

header {
  z-index: 1;
  height: 100px;
}

@import "@/styles/vars.scss";
 ul {
   padding-top: 50px;
   max-height: 100%;

   li {
     display: inline-block;
     line-height: 30px;
     text-transform: uppercase;
   }

   a {
     color: white;
     text-decoration: none;
     transition: 200ms;

     &:hover {
       color: $notWhite;
     }
   }
 }

  img {
    max-height: 30px;
    margin-top: 50px;
  }

  .logo {
    position: relative;

    .underline {
      height: 2px;
      width: 100px;
      background-color: transparent;
      position:absolute;
      bottom: 0px;
      left: 40px;
      transition: 200ms linear;
    }

    &:hover .underline {
      background-color: $myGold;
    }
  }
</style>