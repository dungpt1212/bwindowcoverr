<template>
  <Header />
  <MDBCarousel v-model="carousel" :items="itemsBanners" :indicators="false" class="slide-banner" />
  <div class="about">
    <MDBRow>
      <MDBCol sm="12" md="6">
        <MDBCarousel v-model="carousel" :items="items" :indicators="false"/>
      </MDBCol>
      <MDBCol sm="12" md="6">
        <div class="col-example">
          <p style="font-size: 34px; font-weight: 200;">ABOUT US</p>
          <p class="description">B Window Covers is the family owned business in Melbourne with over 10 years experience and knowledge in the window furnishing industry.</p>
          <p class="description">We manufacture, supply and install a variety range of quality and modern window coverings includes</p>
          <p class="indoor"><a href="#">INDOOR</a></p>
          <p class="indoor"><a href="#">OUTDOOR</a></p>
          <p class="indoor"><a href="#">SECURITY</a></p>
        </div>
      </MDBCol>
    </MDBRow>
  </div>
  <div class="testimonails">
    <MDBRow>
      <MDBCol sm="12" md="6">
        <div class="col-example">
          <div class="special-heading align-center" style="text-align: center;">
            <h4 class="special-h-tag">TESTIMONIALS</h4>
            <!-- <hr class="separator margin-bottom" align="center" style="background-color:red;border-color:red;color:red;height:2px;width:170px;"> -->
          </div>
        </div>
      </MDBCol>
      <MDBCol sm="12" md="6">
        <MDBCarousel v-model="carousel" :items="itemsTeminals" :indicators="false"/>
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
      itemsBanners: [
        {
          src:
            "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide3.jpg",
          interval: 150000,
          alt: "World Class Design",
          label: "WORLD CLASS DESIGN",
          color: "#e81010",
          caption:
            "A job is not complete to us until every single details is taken care of, thats we are rated the best globally",
        },
        {
          src:
            "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide4.jpg",
          interval: 150000,
          alt: "10 Year Experience",
          label: "10 YEAR EXPERIENCE",
          color: "#e81010",
          caption:
            "Simplicity is at the heart of our design, we make complex things look and feel simple",
        },
        {
          src:
            "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide5.jpg",
          interval: 150000,
          alt: "Stunning Window Covers",
          label: "STUNNING WINDOW COVERS",
          color: "#e81010",
          caption:
            "Simplicity is at the heart of our design, we make complex things look and feel simple",
        },
      ],
      items: [
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p3.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p2.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p16.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/p9.jpg",
          interval: 1500,
        },
      ],
      itemsTeminals: [
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/IMG_0018.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/IMG_0019.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/IMG_0020.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/IMG_0016.jpg",
          interval: 1500,
        },
        {
          src: "http://bwindowcovers.com.au/wp-content/uploads/2014/10/IMG_0021.jpg",
          interval: 1500,
        },
      ]
    }
  },
};
</script>

<style lang="scss" scoped>
  .row {
    --mdb-gutter-x: inherit;
  }
  .about {
    padding: 50px 0 0px 0;
    background: #f2f5f8;
    .col-example {
      padding: 60px 30px 60px 60px !important;
      text-align: left;
      .description {
        font-weight: 100;
      }
      h3 {
        margin-bottom: 15px;
        font: 300 31px "Open Sans","Open Sans","Arial",sans-serif;
        color: #222222;
        line-height: 52px;
        text-transform: none;
      }
      .indoor {
        a {
          font-weight: 100;
          color: #d80808 !important;
        }
      }
    }
  }
  .testimonails {
    // padding: 0px 0 40px 0;
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