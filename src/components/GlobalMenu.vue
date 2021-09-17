<template>
  <nav
    class="navbar navbar-fixed-top global-header"
    :class="{ 'scrolled': !showNavbar }"
    id="global-header"
  >
    <div class="container">
      <div class="row">
        <div>
          <div class="navbar-header">
            <button
              type="button"
              data-target="#global-menu"
              id="global-menu-toggler"
              aria-label="global-menu-toggler"
              class="navbar-toggle global-menu-toggle"
              :class="{ 'opened': globalMenuOpen }"
              v-on:click="() => {globalMenuOpen = !globalMenuOpen}"
            >
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
            </button>
            <button
              id="products-menu-toggler"
              type="button"
              data-target="#products-menu"
              aria-label="products-menu"
              class="navbar-toggle products-menu-toggle"
              v-on:click="() => {openWhiteDrop = !openWhiteDrop}"
            ></button>
            <a href class="global-menu-link enter-link">Sign In</a>
            <div
              class="dropdown dropdown-lang"
              :class="{ 'open' : openLang}"
              v-on:click="() => {openLang = !openLang}"
            >
              <button
                type="button"
                id="dropdownMenuButton"
                data-toggle="dropdown"
                aria-haspopup="true"
                aria-expanded="false"
                class="btn btn-secondary dropdown-toggle"
              >en</button>
              <div aria-labelledby="dropdownMenuButton" class="dropdown-menu">
                <li>
                  <a href class="dropdown-item">Ru</a>
                </li>
                <li>
                  <a href class="dropdown-item">Es</a>
                </li>
              </div>
            </div>
          </div>
          <div
            id="global-menu"
            class="navbar-collapse global-menu"
            :class="{ 'in': globalMenuOpen }"
          >
            <ul class="nav navbar-nav">
              <li class="global-menu-item">
                <a href class="global-menu-link">air.io</a>
              </li>
              <li
                class="global-menu-item active"
                v-on:mouseover="() => {openWhiteDrop = true}"
                v-on:mouseout="() => {openWhiteDrop = false}"
              >
                <a href class="global-menu-link">creators ecosystem</a>
              </li>
              <li class="global-menu-item">
                <a href class="global-menu-link">brands</a>
              </li>
              <li class="global-menu-item">
                <a href class="global-menu-link">blog</a>
              </li>
            </ul>
          </div>
          <div
            id="products-menu"
            class="navbar-collapse products-menu"
            :class="{ 'in': openWhiteDrop }"
            v-on:mouseover="() => {openWhiteDrop = true}"
            v-on:mouseout="() => {openWhiteDrop = false}"
          >
            <div class="products-menu-bg">
              <div class="products-menu-row top-row">
                <a href rel="noopener noreferrer" class="sign-in-link">Sign in to AIR CE</a>
                <p class="creators-ecosystem-text">Creators Ecosystem</p>
                <a href class="btn btn-square btn-outline black btn-join">Join AIR</a>
              </div>
              <div class="products-menu-row">
                <div class="col col-l" :class="{ 'light' : col1 }">
                  <p class="menu-title">Packages</p>
                  <ul>
                    <li>
                      <a href class="products-menu-link">Basic Package</a>
                    </li>
                    <li>
                      <a href class="products-menu-link">Grow Faster</a>
                    </li>
                    <li>
                      <a href class="products-menu-link">Earn More</a>
                    </li>
                  </ul>
                </div>
                <div class="col col-c" :class="{ 'light' : col2 }">
                  <p class="menu-title">Channel Types</p>
                  <ul>
                    <li>
                      <a href class="products-menu-link">Kids &amp; Teens</a>
                    </li>
                    <li>
                      <a href class="products-menu-link">Gaming</a>
                    </li>
                  </ul>
                </div>
                <div class="col col-r" :class="{ 'light' : col3 }">
                  <p class="menu-title">Community</p>
                  <ul>
                    <li>
                      <a href class="products-menu-link">AIR Influencer MeetUps</a>
                    </li>
                    <li>
                      <a href class="products-menu-link">AIR Blog</a>
                    </li>
                  </ul>
                </div>
                <div class="col" :class="{ 'light' : col4 }"></div>
              </div>
              <div class="products-menu-row products-items">
                <p class="menu-title">Products</p>
                <ul>
                  <li>
                    <a
                      href
                      class="products-menu-link"
                      v-on:mouseover="() => {col1 = true}"
                      v-on:mouseout="() => {col1 = false}"
                    >AIR Support</a>
                  </li>
                  <li>
                    <a
                      href
                      class="products-menu-link"
                      v-on:mouseover="() => {col2 = true}"
                      v-on:mouseout="() => {col2 = false}"
                    >AIR Ads</a>
                  </li>
                  <li>
                    <a
                      href
                      class="products-menu-link"
                      v-on:mouseover="() => {col3 = true}"
                      v-on:mouseout="() => {col3 = false}"
                    >AIR Distribution</a>
                  </li>
                  <li>
                    <a
                      href
                      class="products-menu-link"
                      v-on:mouseover="() => {
                          if(windowWidth() > 991){
                          col4 = true; 
                          } else {
                          col1 = true
                      }}"
                      v-on:mouseout="() => {
                          if(windowWidth() > 991){
                          col4 = false; 
                          } else {
                          col1 = false;
                      }}"
                    >Translation &amp; Investment</a>
                  </li>
                  <li>
                    <a
                      href
                      class="products-menu-link"
                      v-on:mouseover="() => {
                          if(windowWidth() > 991){
                          col1 = true; 
                          } else {
                          col2 = true
                      }}"
                      v-on:mouseout="() => {
                          if(windowWidth() > 991){
                          col1 = false; 
                          } else {
                          col2 = false;
                      }}"
                    >AIR Pay</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
      openLang: false,
      openWhiteDrop: false,
      globalMenuOpen: false,
      col1: false,
      col2: false,
      col3: false,
      col4: false
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll() {
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop;
      if (currentScrollPosition < 0) {
        return;
      }
      // Stop executing this function if the difference between
      // current scroll position and last scroll position is less than some offset
      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
        return;
      }
      this.showNavbar = currentScrollPosition < this.lastScrollPosition;
      this.lastScrollPosition = currentScrollPosition;
    },
    windowWidth() {
      return window.innerWidth;
    },
    complexHover(firstVal, secondVal, boolean) {
      if (window.innerWidth > 991) {
        firstVal = boolean;
        console.log(firstVal);
      } else {
        secondVal = boolean;
        console.log(secondVal);
      }
    }
  }
};
</script>
W
<style>
.global-header {
  max-height: 42px;
  min-height: 42px;
  background: #1e1e20;
  position: sticky;
  top: 0;
  left: 0;
  z-index: 1000;
}

.global-header {
  transition: all 0.25s ease-out;
}
.global-header.scrolled {
  transform: translateY(-42px);
}

.container {
  max-width: 1200px;
  width: 1170px;
  margin: 0 auto;
  position: relative;
  padding: 0 15px;
  box-sizing: border-box;
}

.navbar-header {
  width: 100%;
  height: 42px;
  display: flex;
  justify-content: space-between;
  padding: 0 0 0 15px;
  box-sizing: border-box;
}

.global-header .products-menu-toggle {
  width: 16px;
  height: 16px;
  border-radius: 8px;
  margin-right: 0;
  margin-top: 11px;
  position: relative;
  z-index: 110;
  -webkit-box-ordinal-group: 4;
  -ms-flex-order: 3;
  order: 3;
  cursor: pointer;
}

.global-header .products-menu-toggle:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background: url(../assets/svgs/products-menu-toggler.svg);
  background-position: 50%;
  background-size: contain;
  background-repeat: no-repeat;
  z-index: 20;
}

.navbar-toggle {
  position: relative;
  float: right;
  padding: 9px 10px;
  margin-right: 15px;
  margin-top: 8px;
  margin-bottom: 8px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 4px;
}

.global-header .dropdown-lang {
  position: relative;
  display: inline-block;
  order: 2;
  align-self: center;
  margin-left: auto;
  z-index: 20;
  margin-right: 15px;
}

.global-header .dropdown-lang .dropdown-toggle {
  background-color: transparent;
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 16px;
  color: #fff;
  opacity: 0.8;
  text-transform: lowercase;
  position: relative;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  padding: 6px 12px 6px 6px;
}

.global-header .dropdown-lang .dropdown-toggle:after {
  content: "";
  background: url(../assets/svgs/arrow-down.svg);
  background-size: contain;
  background-repeat: no-repeat;
  background-position: 50%;
  top: 12px;
  right: 0;
  width: 8px;
  height: 5px;
  display: inline-block;
  -webkit-transform: translate(0);
  transform: translate(0);
  position: absolute;
}

.global-header .dropdown-lang.open .dropdown-toggle {
  padding: 6px 12px 6px 6px;
  position: relative;
}

.navbar-header .enter-link {
  display: none;
  font-family: Gilroy, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
  color: #fff;
  opacity: 0.8;
  text-transform: lowercase;
  position: absolute;
  right: 95px;
  top: 50%;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  font-size: 14px;
  text-align: left;
  list-style: none;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  box-shadow: 0 6px 12px rgb(0 0 0 / 18%);
}

.global-header .dropdown-lang.open .dropdown-menu {
  background-color: #1e1e20;
  min-width: 20px;
  border: 0;
  margin-top: 4px;
  border-radius: 0;
  height: 50px;
}

.open > .dropdown-menu {
  display: block;
}

.global-header .dropdown-lang.open .dropdown-item {
  color: #fff;
  opacity: 0.8;
  padding: 3px 16px 3px 13px;
  text-transform: lowercase;
  font-weight: 700;
  letter-spacing: 0.02em;
  line-height: 2;
}

.global-header .dropdown-lang.open .dropdown-item:hover {
  color: #fff;
  text-decoration: none;
  background-color: #6f2aae;
}

.global-menu {
  width: auto;
  background: transparent;
  position: absolute;
  display: none;
  top: 0;
  left: 0;
  clear: both;
  min-height: auto;
  display: none;
  min-height: 100vh;
  background-color: #28282b;
  z-index: 100;
  width: 100%;
}

.global-menu.in {
  display: flex;
  justify-content: center;
  align-items: baseline;
  top: 42px;
}

.global-header .global-menu-toggle {
  border: 0;
  float: left;
  position: absolute;
  left: 15px;
  width: 17px;
  padding: 0;
  margin-right: 14px;
  margin-top: 13px;
  height: 15px;
  cursor: pointer;
  border-radius: 0 !important;
}

.global-header .global-menu-toggle .icon-bar {
  display: block;
  border: 0;
  height: 2px;
  background-color: #fff;
  width: 17px;
  border-radius: 0;
  transition: all 0.25s ease-out;
}

.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}

.global-header .global-menu-toggle.opened .icon-bar:first-of-type {
  transform: rotate(45deg) translate(4px, 4px);
  transition: all 0.25s ease-out;
}

.global-header .global-menu-toggle.opened .icon-bar:nth-of-type(2) {
  width: 0;
  transition: all 0.25s ease-out;
}

.global-header .global-menu-toggle.opened .icon-bar:nth-of-type(3) {
  transform: rotate(-45deg) translate(4px, -4px);
  transition: all 0.25s ease-out;
}

.global-menu .navbar-nav {
  top: 0;
  left: 0;
  display: flex;
  /* margin: 0; */
  max-height: 42px;
  list-style: none;
  padding: 0;
  align-self: center;
  margin: -100.5px -15px 0;
  flex-direction: column;
}

.global-menu .navbar-nav li {
  padding-left: 32px;
  padding-right: 32px;
  padding-bottom: 13px;
  padding-top: 13px;
}

.global-menu li:hover {
  background-color: #131315;
}

.global-menu .global-menu-link {
  font-family: Gilroy, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 22px !important;
  line-height: 26px;
  text-align: center;
  color: #fff !important;
  opacity: 0.8 !important;
  text-transform: none !important;
  padding-top: 20px;
  padding-bottom: 20px;
}

.navbar .navbar-collapse.products-menu {
    overflow-x: hidden;
    position: absolute;
    left: 0;
    width: 100%;
    top: 42px;
    box-sizing: border-box;
    height: 100%;
}

.products-menu {
    display: none!important;
    /* background-color: #f0f8ff; */
    color: #1e1e20;
    padding: 28px 15px;
    z-index: 100;
    min-height: 100vh;
}

.products-menu.in {
    display: block !important;
    overflow-y: auto;
}

.products-menu-bg {
    position: relative;
    height: 100%;
    width: 100%;
}

.products-menu-bg:before {
    content: "";
    position: absolute;
    left: 50%;
    top: -30px;
    transform: translate(-50%);
    width: 400%;
    height: 200%;
    background-color: #fff;
    z-index: -1;
    box-shadow: 0 23px 47px -17px rgb(59 68 92 / 12%);
}

.products-menu-row {
  text-align: left;
}

.products-menu-row:first-of-type {
  border-top: 0;
}

.products-menu .products-menu-row.products-items {
  display: block;
}

.products-menu .sign-in-link {
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    color: #1e1e20;
    padding-left: 32px;
    position: relative;
}

.products-menu .sign-in-link:before {
  content: "";
  position: absolute;
  left: 0;
  top: 50%;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
  width: 15px;
  height: 20px;
  background: url(../assets/svgs/header-nav-link.svg);
  background-size: contain;
  background-position: 50%;
  background-repeat: no-repeat;
}

.products-menu .btn-join {
  border: 2px solid #000;
  display: none;
}

.products-menu .products-menu-row.top-row {
    padding-top: 0;
    margin-bottom: 35px;
    padding-bottom: 0;
    border: none;
}

.products-menu .products-menu-row.top-row .creators-ecosystem-text {
  display: none;
}

.products-menu .products-menu-row {
  border-top: 1px solid #dadada;
  padding-top: 26px;
  padding-bottom: 36px;
}

.products-menu .menu-title {
  font-style: normal;
  font-weight: 500;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #3b3b3b;
  opacity: 0.6;
  margin-bottom: 21px;
}

.products-menu .col:last-of-type {
  display: none;
}

.products-menu ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.products-menu li {
  list-style: none;
  margin: 0;
  padding-bottom: 12px;
}

.products-menu-link {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 38px;
  color: #1e1e20;
}

.products-menu-link:hover {
  color: #000;
  font-weight: 600;
}

@media (min-width: 768px) {
  .global-menu {
    display: inline-block !important;
    min-height: initial;
    width: auto;
    background: transparent;
    position: absolute;
    top: 0;
    display: inline-block !important;
    clear: both;
    min-height: auto;
  }

  .global-menu .navbar-nav {
    margin: 0;
    flex-direction: row;
  }

  .global-menu .navbar-nav li {
    padding-left: 22px;
    padding-right: 22px;
  }

  .global-menu .navbar-nav li.active {
    background-color: #131315;
    color: #fff;
  }

  .global-menu .global-menu-link {
    top: 0;
    left: 0;
    padding: 0;
    font-size: 14px !important;
    line-height: 16px !important;
  }

  .global-menu-toggle {
    display: none;
  }
  .global-header .products-menu-toggle {
    display: block !important;
  }

  .navbar .navbar-collapse {
    top: 0;
  }

  .navbar .navbar-collapse.products-menu{
    height: auto;
  }

  .products-menu {
    padding-top: 30px;
    overflow: visible!important;
}

  .products-menu-bg:before {
    top: -30px;
    height: calc(100% + 55px);
  }

  .products-menu .products-menu-row.top-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-height: 95px;
    margin-bottom: 25px;
    padding: 0;

    height: 42px;
  }

  .products-menu .products-menu-row {
    border-top: none;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
  }

  .products-menu .btn-join {
    font-size: 13px;
    line-height: 12px;
    display: inline-block;
    padding: 11px 25px;
    border: 2px solid #000;
    border-radius: 7px;
    font-weight: 700;
    text-transform: uppercase;
    color: #000;
    -webkit-transition: all 0.3s ease-out;
    transition: all 0.3s ease-out;
    background-color: transparent;
  }

  .products-menu .btn-join:hover {
    background: #000;
    color: #fff !important;
    border: 2px solid #000;
  }

  .products-menu .col {
    margin-bottom: 0;
    width: calc(33.333% - 5px);
    margin-right: 5px;
    position: relative;
  }

  .products-menu .col:before {
    content: "";
    height: 2px;
    width: 100%;
    position: absolute;
    top: -26px;
    left: 0;
    background-color: #e5e5e5;
    -webkit-transition: 0.3s;
    transition: 0.3s;
  }

  .products-menu .col.light:before {
    background-color: #000;
    transition: 0.3s;
  }

  .products-menu .col:hover:before {
    background-color: #000;
    -webkit-transition: 0.3s;
    transition: 0.3s;
  }

  .products-menu .products-menu-row.products-items ul {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
  }

  .products-menu .products-menu-row.products-items li {
    width: calc(33.333% - 5px);
    margin-right: 5px;
    margin-bottom: 0;
    padding-bottom: 12px;
  }
}

@media (min-width: 992px) {
  .products-menu {
    padding: 26px 15px !important;
  }

  .products-menu-bg:before {
    top: -26px;
  }

  .products-menu .products-menu-row {
    padding-top: 44px;
  }
  .products-menu .products-menu-row.products-items {
    padding-top: 0;
  }

  .products-menu .btn-join {
    padding: 13px 26px;
    font-size: 16px;
  }

  .products-menu .products-menu-row {
    padding-top: 44px;
  }

  .products-menu .products-menu-row {
    padding-top: 44px;
  }

  .products-menu .menu-title {
    margin-bottom: 27px;
  }

  .products-menu .col:last-of-type {
    display: block !important;
  }

  .products-menu .col:before {
    top: -44px;
    height: 3px;
  }

  .products-menu .products-menu-row.products-items {
    padding-top: 0;
  }

  .products-menu .products-menu-row.products-items li {
    width: calc(25% - 5px);
    margin-right: 5px;
  }
}

@media (min-width: 1200px) {
  .navbar-header .enter-link {
    display: inline-block;
  }

  .global-header .products-menu-toggle {
    display: none !important;
    z-index: 5;
    position: relative;
  }

  .global-header .dropdown-lang {
    margin-right: 0;
  }

  .products-menu .sign-in-link {
    display: none;
  }

  .products-menu .products-menu-row.top-row .creators-ecosystem-text {
    display: block;
    font-family: Gilroy;
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 28px;
    color: #3b3b3b;
  }
}
</style>