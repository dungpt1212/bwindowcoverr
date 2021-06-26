<template>
  <header>
    <!-- Navbar -->
    <!-- PC -->
    <MDBNavbar v-if="screenSize >= 992" expand="lg" light bg="white" container position="sticky">
      <MDBNavbarNav collapse="navbarExample01" class="mb-2 mb-lg-0" center>
        <MDBNavbarItem to="#" class="pt-3 w-100px" :class="{ menu_active: $route.name == 'Home' }">
          <router-link to="/"> HOME </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem 
          to="#" 
          class="pt-3 pr-5 w-100px product" 
          @mouseover="showSubMenu" 
          @mouseleave="hideSubMenu"
        > 
          <span :class="{ menu_active: $route.name == 'Indoor' || $route.name == 'Outdoor' || $route.name == 'Security' }">product</span> 
          <ul v-if="showSubMenuFlag" class="sub-menu clearfix">
            <li :class="{ menu_active: $route.name == 'Indoor'}">
              <a href="/indoor">
                <router-link to="/indoor"> INDOOR </router-link>
              </a>
            </li>
            <li :class="{ menu_active: $route.name == 'Outdoor'}">
              <a href="/outdoor">
                <router-link to="/outdoor"> OUTDOOR </router-link>
              </a>
            </li>
            <li :class="{ menu_active: $route.name == 'Security'}">
              <a href="/security">
                <router-link to="/security"> SECURITY </router-link>
              </a>
            </li>
          </ul>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="w-300px">
          <router-link to="/"> <img src="@/assets/logo.png"> </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px" :class="{ menu_active: $route.name == 'Gallery' }"> 
          <router-link to="/gallery"> GALLERY </router-link>
        </MDBNavbarItem>
        <MDBNavbarItem to="#" class="pt-3 w-100px" :class="{ menu_active: $route.name == 'Contact' }"> 
          <router-link to="/contact"> CONTACT </router-link>
        </MDBNavbarItem>
      </MDBNavbarNav>
    </MDBNavbar>

    <!-- Mobile, Ipad -->
    <MDBNavbar v-if="screenSize < 992" expand="lg" light bg="white" container position="sticky">
      <!-- <img src="@/assets/logo.png" style="margin-left:10%"> -->
      <router-link to="/"> <img src="@/assets/logo.png" style="margin-left:10%"> </router-link>
      <button 
        class="navbar-toggler btn-navbar-toggler" 
        type="button"
        @click="handleShowMobileMenu"
      >
        <i class="fas fa-bars"></i>
      </button>
      <MDBListGroup>
        <MDBListGroupItem tag="a" :class="{ menu_active: $route.name == 'Home' }" action>
          <router-link to="/"> Home </router-link>
        </MDBListGroupItem>
        <MDBListGroupItem 
          tag="a" 
          action 
          @click="handleShowMobileSubMenu" 
          style="cursor: pointer;"
        >
          <span :class="{ menu_active: $route.name == 'Indoor' || $route.name == 'Outdoor' || $route.name == 'Security' }">Products</span>
          <span class="fas fa-angle-right mobile-submenu-btn" style="font-size: 12px;float:right;margin-top:-8px;padding:15px;margin-right:-15px;"></span>
          <ul style="list-style:none" class="mobile-submenu">
            <li :class="{ menu_active: $route.name == 'Indoor' }">
              <router-link to="/indoor"> indoor </router-link>
            </li>
            <li :class="{ menu_active: $route.name == 'Outdoor' }">
              <router-link to="/outdoor"> outdoor </router-link>
            </li>
            <li :class="{ menu_active: $route.name == 'Security' }">
              <router-link to="/security"> security </router-link>
            </li>
          </ul>
        </MDBListGroupItem>
        <MDBListGroupItem :class="{ menu_active: $route.name == 'Gallery' }" tag="a" action>
          <router-link to="/gallery"> Gallery </router-link>
        </MDBListGroupItem>
        <MDBListGroupItem :class="{ menu_active: $route.name == 'Contact' }" tag="a" action>
          <router-link to="/contact"> Contract </router-link>
        </MDBListGroupItem>
      </MDBListGroup>
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
  //MDBNavbarToggler,
  MDBNavbarNav,
  MDBNavbarItem,
  MDBListGroup, 
  MDBListGroupItem
} from "mdb-vue-ui-kit";
import $ from 'jquery'

export default {
  name: "Header",
  components: {
    // MDBBtn,
    MDBNavbar,
    //MDBNavbarToggler,
    MDBNavbarNav,
    MDBNavbarItem,
    MDBListGroup,
    MDBListGroupItem
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
    window.addEventListener("resize", this.handleResponsive);
  },
  data() {
    return {
      scrollPosition: 0,
      showSubMenuFlag: false,
      screenSize: 0,
      showMobileMenu: false,
      showMobileSubMenu: false,
    }
  },
  methods: {
    handleScroll () {
      this.scrollPosition = window.scrollY;
      var element = document.querySelector('nav.navbar.navbar-light.bg-white.navbar-expand-lg.sticky-top');
      if (this.screenSize > 992) {
        if (this.scrollPosition >= 120 && this.scrollPosition < 230) {
          element.classList.remove('down');
          element.classList.remove('down2');
          element.classList.add('up');   
        } else if (this.scrollPosition >= 230) {
          element.classList.remove('up');
          element.classList.remove('down');
          element.classList.add('down2'); 
        } else {
          element.classList.remove('up');
          element.classList.remove('down2');
          if (this.$route.name == 'Gallery') {
            element.classList.add('down2'); 
          } else {
            element.classList.add('down'); 
          }
        }
      }
    },
    showSubMenu () {
      this.showSubMenuFlag = true;
    },
    hideSubMenu () {
      this.showSubMenuFlag = false;
    },
    handleResponsive () {
      this.screenSize = window.innerWidth;
    },
    handleShowMobileMenu () {
      this.showMobileMenu = !this.showMobileMenu;
      if (this.showMobileMenu) {
        $('ul.list-group').slideDown();
      } else {
        $('ul.list-group').slideUp();
      }
    },
    handleShowMobileSubMenu () {
      this.showMobileSubMenu = !this.showMobileSubMenu;
      if (this.showMobileSubMenu) {
        $('ul.mobile-submenu').slideDown();
        $('.mobile-submenu-btn').removeClass('fa-angle-right');
        $('.mobile-submenu-btn').addClass('fa-angle-down');
      } else {
        $('ul.mobile-submenu').slideUp();
        $('.mobile-submenu-btn').removeClass('fa-angle-down');
        $('.mobile-submenu-btn').addClass('fa-angle-right');
      }
    }
  },
  mounted() {
    this.handleScroll();
    this.handleResponsive();  
  },
};
</script>

<style lang="scss">
  .slide-banner {
    .carousel-inner {
      // height: 100vh;
      img {
        max-height: 100vh;
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
  .list-group-item-action {
    border-bottom: 1px solid #eaeaea;
    a {
      color: #262626;
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
      font-size: 17px;
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
    span.menu_active {
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
    .btn-navbar-toggler {
      position: fixed;
      right: 10%;
      top: 20px;
      color: white;
    }
    ul.list-group {
      position: absolute;
      top: 100px;
      left: 0px;
      width: 100%;
      text-align: left;
      display: none;
      a {
        font-weight: 100;
        text-transform: uppercase;
        font-size: 14px;
      }
      ul.mobile-submenu {
        display: none;
        margin-top: 12px;
        li {
          margin-bottom: 5px;
        }
      }
      a:hover {
        color: black !important;
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
  .list-group-item-action:hover, .list-group-item-action:focus {
    background-color: white;
  }
</style>