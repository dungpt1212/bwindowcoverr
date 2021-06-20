<template>
  <header>
    <!-- Navbar -->
    <MDBNavbar expand="lg" light bg="white" container position="sticky">
      <MDBNavbarToggler target="#navbarExample01"></MDBNavbarToggler>
      <MDBNavbarNav collapse="navbarExample01" class="mb-2 mb-lg-0" center>
        <MDBNavbarItem to="#" class="pt-3 w-100px menu_active"> Home </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 pr-5 w-100px product" @mouseover="showSubMenu" @mouseleave="hideSubMenu"> 
          Products 
          <ul v-if="showSubMenuFlag" class="sub-menu clearfix">
            <li><a href="/indoor">INDOOR</a></li>
            <li><a href="/indoor">OUTDOOR</a></li>
            <li><a href="/indoor">SECURITY</a></li>
          </ul>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="w-300px">
          <img src="http://bwindowcovers.com.au/wp-content/uploads/2016/07/BWClogo.png">
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px"> Gallery </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px"> Contact </MDBNavbarItem>
      </MDBNavbarNav>
    </MDBNavbar>
    <!-- Navbar -->

    <!-- Background image -->
    <!-- <div
      class="p-5 text-center bg-image"
      style="
        background-image: url('http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide3.jpg');
        height: 700px;
      "
    >
      <div class="mask" style="background-color: rgba(0, 0, 0, 0.2)">
        <div class="d-flex justify-content-center align-items-center h-100">
          <div class="text-white">
            <h1 class="mb-3">Heading</h1>
            <h4 class="mb-3">Subheading</h4>
            <MDBBtn tag="a" lg outline="light" href="#!" role="button"
              >Call to action
            </MDBBtn>
          </div>
        </div>
      </div>
    </div> -->
    <!-- Background image -->

    <!-- Carousel -->
    <MDBCarousel v-model="carousel" :items="items" :indicators="false" class="slide-banner" />
  </header>
</template>

<script>
import { ref } from "vue";
import {
  //   MDBBtn,
  MDBNavbar,
  MDBNavbarToggler,
  MDBNavbarNav,
  MDBNavbarItem,
  MDBCarousel,
} from "mdb-vue-ui-kit";
export default {
  name: "Header",
  components: {
    // MDBBtn,
    MDBNavbar,
    MDBNavbarToggler,
    MDBNavbarNav,
    MDBNavbarItem,
    MDBCarousel,
  },
  setup() {
    const items = [
      {
        src:
          "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide3.jpg",
        interval: 1500,
        alt: "World Class Design",
        label: "WORLD CLASS DESIGN",
        caption:
          "A job is not complete to us until every single details is taken care of, thats we are rated the best globally",
      },
      {
        src:
          "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide4.jpg",
        interval: 1500,
        alt: "10 Year Experience",
        label: "10 YEAR EXPERIENCE",
        caption:
          "Simplicity is at the heart of our design, we make complex things look and feel simple",
      },
      {
        src:
          "http://bwindowcovers.com.au/wp-content/uploads/2016/07/slide5.jpg",
        interval: 1500,
        alt: "Stunning Window Covers",
        label: "STUNNING WINDOW COVERS",
        caption:
          "Simplicity is at the heart of our design, we make complex things look and feel simple",
      },
    ];
    const carousel = ref(0);

    return {
      items,
      carousel,
    };
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  data() {
    return {
      scrollPosition: 0,
      showSubMenuFlag: false,
    }
  },
  methods: {
    handleScroll () {
      this.scrollPosition = window.scrollY;
      var element = document.querySelector('nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top');
      if (this.scrollPosition >= 120 && this.scrollPosition < 595) {
        element.classList.remove('down');
        element.classList.remove('down2');
        element.classList.add('up');   
      } else if (this.scrollPosition >= 595) {
        element.classList.remove('up');
        element.classList.remove('down');
        element.classList.add('down2'); 
      } else {
        element.classList.remove('up');
        element.classList.remove('down2');
        element.classList.add('down'); 
      }
    },
    showSubMenu () {
      this.showSubMenuFlag = true;
    },
    hideSubMenu () {
      this.showSubMenuFlag = false;
    }
  },
  mounted() {
    this.handleScroll();
  },
};
</script>

<style lang="scss">
  .slide-banner {
    .carousel-inner {
      height: 100vh;
      img {
        height: 100vh;
      }
      .carousel-caption {
        bottom: 40%;
      }
    }
    .carousel-indicators {
      bottom: 35%;
    }
  }
  nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top {
    background: rgba(0,0,0,0.4) !important;
    position: fixed;
    width: 100%;
    height: 100px;
    a.router-link-active.router-link-exact-active.nav-link {
      color: #ffffff;
      text-transform: uppercase;
      font-size: 13px;
      font-weight: 100;
    }
    .w-300px {
      width: 300px;
    }
    .w-100px {
      width: 100px;
    }
    .menu_active a {
      color: #d80808 !important;
    }
    a:hover {
      color: #d80808 !important;
    }
    li.product {
      position: relative;
    }
    ul.sub-menu {
      width: 200px;
      background: rgba(0,0,0,0.62);
      position: absolute;
      top: 70px;
      left: -15px;
      display: block;
      list-style: unset;
      padding-top: 15px;
      padding-bottom: 15px;
      li {
        text-align: left;
        line-height: 35px;
        a {
          color: white;
        }
      }
    }
  }
  .product:hover .sub-menu {
    display: block;
  }
  nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top.up {
    top: -200px;
    transition: 1s;
  }
  nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top.down {
    top: 0px;
    transition: 1s;
  }
  nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top.down2 {
    top: 0px;
    transition: 2s;
    background: #bfbfbf !important;
  }
</style>