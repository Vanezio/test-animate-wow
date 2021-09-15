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
            <!-- <button
              type="button"
              data-target="#global-menu"
              id="global-menu-toggler"
              aria-label="global-menu-toggler"
              class="navbar-toggle global-menu-toggle"
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
            ></button>-->
            <a href="https://my.air.io/#/account/login" class="global-menu-link enter-link">Sign In</a>
            <div class="dropdown dropdown-lang" :class="{ 'open' : openLang}" v-on:click="langToggle">
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
                  <a href="https://air.io/ce/basic" class="dropdown-item">Ru</a>
                </li>
                <li>
                  <a href="https://air.io/es/ce/basic" class="dropdown-item">Es</a>
                </li>
              </div>
            </div>
          </div>
          <div id="global-menu" class="navbar-collapse global-menu">
            <ul class="nav navbar-nav">
              <li class="global-menu-item">
                <a href="https://air.io/en" class="global-menu-link">air.io</a>
              </li>
              <li class="global-menu-item active">
                <a href="https://air.io/en/ce" class="global-menu-link">creators ecosystem</a>
              </li>
              <li class="global-menu-item">
                <a href="https://brands.air.io" class="global-menu-link">brands</a>
              </li>
              <li class="global-menu-item">
                <a href="https://air.io/en/blog" class="global-menu-link">blog</a>
              </li>
            </ul>
          </div>
          <!-- <div id="products-menu" class="navbar-collapse products-menu">
          <div class="products-menu-bg">-->
          <!-- <div class="products-menu-row top-row">
                <a
                  href="https://my.air.io/#/account/login"
                  rel="noopener noreferrer"
                  class="sign-in-link"
                >Sign in to AIR CE</a>
                <p class="creators-ecosystem-text">Creators Ecosystem</p>
                <a
                  href="https://my.air.io/#/account/registration"
                  class="btn btn-square btn-outline black btn-join"
                >Join AIR</a>
          </div>-->
          <!-- <div class="products-menu-row">
                <div class="col col-l">
                  <p class="menu-title">Packages</p>
                  <ul>
                    <li>
                      <a href="https://air.io/en/ce/basic" class="products-menu-link">Basic Package</a>
                    </li>
                    <li>
                      <a
                        href="https://air.io/en/ce/grow-faster"
                        class="products-menu-link"
                      >Grow Faster</a>
                    </li>
                    <li>
                      <a href="https://air.io/en/ce/earn-more" class="products-menu-link">Earn More</a>
                    </li>
                  </ul>
                </div>
                <div class="col col-c">
                  <p class="menu-title">Channel Types</p>
                  <ul>
                    <li>
                      <a
                        href="https://air.io/en/ce/kids-and-teens"
                        class="products-menu-link"
                      >Kids &amp; Teens</a>
                    </li>
                    <li>
                      <a href="https://air.io/en/ce/gaming" class="products-menu-link">Gaming</a>
                    </li>
                  </ul>
                </div>
                <div class="col col-r">
                  <p class="menu-title">Community</p>
                  <ul>
                    <li>
                      <a href="https://im.air.io/" class="products-menu-link">AIR Influencer MeetUps</a>
                    </li>
                    <li>
                      <a href="https://air.io/en/blog" class="products-menu-link">AIR Blog</a>
                    </li>
                  </ul>
                </div>
                <div class="col"></div>
          </div>-->
          <!-- <div class="products-menu-row products-items">
                <p class="menu-title">Products</p>
                <ul>
                  <li>
                    <a href="https://air.io/en/ce/support" class="products-menu-link">AIR Support</a>
                  </li>
                  <li>
                    <a href="https://air.io/en/ce/ads" class="products-menu-link">AIR Ads</a>
                  </li>
                  <li>
                    <a
                      href="https://air.io/en/ce/distribution"
                      class="products-menu-link"
                    >AIR Distribution</a>
                  </li>
                  <li>
                    <a
                      href="https://translate.air.io"
                      class="products-menu-link"
                    >Translation &amp; Investment</a>
                  </li>
                  <li>
                    <a href="https://air.io/en/ce/pay" class="products-menu-link">AIR Pay</a>
                  </li>
                </ul>
          </div>-->
          <!-- </div>
          </div>-->
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
      openLang: false
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
    langToggle() {
        this.openLang = !this.openLang
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

.global-header .dropdown-lang {
  position: relative;
  display: inline-block;
  order: 2;
  align-self: center;
  margin-left: auto;
  z-index: 20;
  margin-right: 0;
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
  display: inline-block;
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

.open>.dropdown-menu {
    display: block;
}

.global-header .dropdown-lang.open .dropdown-item {
    color: #fff;
    opacity: .8;
    padding: 3px 16px 3px 13px;
    text-transform: lowercase;
    font-weight: 700;
    letter-spacing: .02em;
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
  top: 0;
  left: 0;
  display: inline-block !important;
  clear: both;
  min-height: auto;
}

.global-menu .navbar-nav {
  top: 0;
  left: 0;
  display: flex;
  margin: 0;
  max-height: 42px;
  list-style: none;
      padding: 0;
}

.global-menu .navbar-nav li {
  padding-left: 32px;
  padding-right: 32px;
  padding-bottom: 13px;
  padding-top: 13px;
}

.global-menu .navbar-nav li.active {
  background-color: #131315;
  color: #fff;
}

.global-menu li:hover {
  background-color: #131315;
}

.global-menu .global-menu-link {
  top: 0;
  left: 0;
  padding: 0;
  font-size: 14px !important;
  line-height: 16px !important;
  font-weight: 400;
  text-align: center;
  color: #fff !important;
  opacity: 0.8 !important;
  text-transform: none !important;
}
</style>