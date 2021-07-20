<template>
  <a href="#elevate-here" id="elevator">
      <i class="fas fa-chevron-up clear"></i>
      <p>
          top
      </p>
  </a>
</template>

<script>
export default {
    name: "Elevator"
}
</script>

<style scoped lang="scss">

    @import "@/styles/vars.scss";

    #elevator {
        background-color: $myBGBlue4;
        color: white;
        width: 70px;
        height: 70px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        
        i {
            margin-top: 15px;
        }

        p {
            text-transform: uppercase;
            font-weight: 600;
        }
    }
</style>