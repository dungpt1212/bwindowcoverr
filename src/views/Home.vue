<template>
  <Header />
  <div class="about">
    <MDBRow>
      <MDBCol>
        <MDBCarousel v-model="carousel" :items="items" :indicators="false"/>
      </MDBCol>
      <MDBCol>
        <div class="col-example">
          <h3>ABOUT US</h3>
          <p>B Window Covers is the family owned business in Melbourne with over 10 years experience and knowledge in the window furnishing industry.</p>
          <p>We manufacture, supply and install a variety range of quality and modern window coverings includes</p>
          <p class="indoor"><a>INDOOR</a></p>
          <p class="indoor"><a>OUTDOOR</a></p>
          <p class="indoor"><a>SECURITY</a></p>
        </div>
      </MDBCol>
    </MDBRow>
  </div>
  <div class="testimonails">
    <MDBRow>
      <MDBCol>
        <div class="col-example">
          <div class="special-heading align-center" style="text-align: center;">
            <h4 class="special-h-tag">TESTIMONIALS</h4>
            <hr class="separator margin-bottom" align="center" style="background-color:red;border-color:red;color:red;height:2px;width:170px;">
          </div>
        </div>
      </MDBCol>
      <MDBCol>
        <MDBCarousel v-model="carousel" :items="items" :indicators="false"/>
      </MDBCol>
    </MDBRow>
  </div>
  <Footer />
</template>
<script>
import Header from "@/views/Header.vue";
import Footer from "@/views/Footer.vue";
import { MDBCol, MDBRow, MDBCarousel} from 'mdb-vue-ui-kit'
export default {
  name: "Home",
  components: { Header, Footer, MDBCol, MDBRow, MDBCarousel },
  data() {
    return {
      items: [
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p3.jpg",
          interval: 5000,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p2.jpg",
          interval: 5000,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p16.jpg",
          interval: 5000,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p9.jpg",
          interval: 5000,
        },
      ]
    }
  },
};
</script>

<style lang="scss" scoped>
  .about {
    padding: 50px 0 40px 0;
    background: #f2f5f8;
    .col-example {
      padding: 10px 50px 10px 20px;
      text-align: left;
      h3 {
        margin-bottom: 15px;
        font: 300 31px "Open Sans","Open Sans","Arial",sans-serif;
        color: #222222;
        line-height: 52px;
        text-transform: none;
      }
      .indoor {
        color: #d80808;
      }
    }
  }
  .testimonails {
    padding: 30px 0 40px 0;
    .col-example {
      padding: 10px 50px 10px 20px;
      h3 {
        margin-bottom: 15px;
        font: 300 31px "Open Sans","Open Sans","Arial",sans-serif;
        color: #222222;
        line-height: 52px;
        text-transform: none;
      }
      .indoor {
        color: #d80808;
      }
    }
  }
</style>