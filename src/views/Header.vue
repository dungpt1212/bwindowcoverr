<template>
  <div class="header">
    <div class="header-inner-wrap">
      <div class="header-wrap">
        <div class="logo">
          <a href="www.bwindowcovers.com.au">
            <img src="../assets/BWClogo_W.png" alt="" />
          </a>
        </div>
      </div>
    </div>
    <Carousel v-bind:hero-images="['hello', 'world']" />
  </div>
</template>

<script>
import Carousel from "@/components/Carousel.vue";
export default {
  name: "Header",
  components: {
    Carousel
  },
};
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  z-index: 10;
  display: block;
  .header-inner-wrap {
    width: 100%;
    position: absolute;
    //transition: background .25s ease, box-shadow .25s ease;
    background-color: rgba(0, 0, 0, 0.4);
    .header-wrap {
      box-shadow: none;
      background: transparent;
      text-align: center;
      line-height: 70px;
    }
  }
}
</style>