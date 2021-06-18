<template>
  <div>
    <MDBFooter>
      <div class="footer">
        Copyright B Window Covers 2016. All Rights Reserved					
      </div>
    </MDBFooter>
  </div>
</template>

<script>
import { MDBFooter } from 'mdb-vue-ui-kit';
export default {
  name: "Footer",
  components: {
    MDBFooter
  },
};
</script>

<style lang="scss" scoped>
  .footer {
    background: #2c2e2e;
    padding-top: 30px;
    padding-bottom: 30px;
    text-align: left;
    color: #808080;
    font-size: 14px;
    padding-left: 30px;
  }
</style>