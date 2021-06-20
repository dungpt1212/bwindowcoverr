<template>
  <header>
    <!-- Navbar -->
    <MDBNavbar expand="lg" light bg="white" container position="sticky">
      <MDBNavbarToggler target="#navbarExample01"></MDBNavbarToggler>
      <MDBNavbarNav collapse="navbarExample01" class="mb-2 mb-lg-0" center>
        <MDBNavbarItem to="#" class="pt-3 w-100px menu_active">
          <router-link to="/"> HOME </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 pr-5 w-100px product" @mouseover="showSubMenu" @mouseleave="hideSubMenu"> 
          PRODUCTS 
          <ul v-if="showSubMenuFlag" class="sub-menu clearfix">
            <li><a href="/indoor">
              <router-link to="/indoor"> INDOOR </router-link>
            </a></li>
            <li><a href="/indoor">
              <router-link to="/outdoor"> OUTDOOR </router-link>
            </a></li>
            <li><a href="/indoor">
              <router-link to="/outdoor"> SECURITY </router-link>
            </a></li>
          </ul>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="w-300px">
          <router-link to="/"> <img src="http://bwindowcovers.com.au/wp-content/uploads/2016/07/BWClogo.png"> </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px"> 
          <router-link to="/gallery"> GALLERY </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px"> 
          <router-link to="/contact"> CONTACT </router-link>
        </MDBNavbarItem>
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

  </header>
</template>

<script>
import {
  //   MDBBtn,
  MDBNavbar,
  MDBNavbarToggler,
  MDBNavbarNav,
  MDBNavbarItem,
} from "mdb-vue-ui-kit";
export default {
  name: "Header",
  components: {
    // MDBBtn,
    MDBNavbar,
    MDBNavbarToggler,
    MDBNavbarNav,
    MDBNavbarItem,
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
      // height: 100vh;
      img {
        // height: 100vh;
      }
      .carousel-caption {
        bottom: 50%;
        h5 {
          font-size: 40px;
          // color: #4e4d4d;
        }
        p {
          // color: #4e4d4d;
          font-size: 17px;
        }
      }
    }
    .carousel-indicators {
      bottom: 35%;
    }
  }
  nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top {
    background: #bfbfbf !important;
    position: fixed;
    width: 100%;
    height: 100px;
    a.router-link-active.router-link-exact-active.nav-link {
      color: #ffffff;
      text-transform: uppercase;
      font-size: 14px;
      font-weight: 100;
      a {
        color: #ffffff;
      }
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