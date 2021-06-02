<template>
  <Header />
  <div class="content">
    
  </div>
  <Footer />
</template>
<script>
import Header from "@/views/Header.vue";
import Footer from "@/views/Footer.vue";
export default {
  name: "Home",
  components: { Header, Footer },
  //   setup(props, ctx) {

  //   },
};
</script>

<style lang="scss" scoped>
.content {
  margin: 0;
}
</style>