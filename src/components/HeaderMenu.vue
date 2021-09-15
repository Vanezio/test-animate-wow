<template>
  <nav class="navbar local-menu navbar-fixed-top page-menu transparent animate__fadeInDown" :class="{ 'not-at-top': notAtTop }">
    <div class="container">
      <div class="page-menu-wrapper">
        <a href="#about" aria-label="about" class="page-menu-logo">
          <img src="../assets/svgs/logo.svg" alt="">
        </a>
        <ul class="page-menu-list">
          <li class="page-menu-item">
            <a href="#about" class="page-menu-link">About</a>
          </li>
          <li class="page-menu-item">
            <a href="#creators-ecosystem" class="page-menu-link">Creators Ecosystem</a>
          </li>
          <li class="page-menu-item">
            <a href="#services" class="page-menu-link">
              What's inside
              <span class="icon-count">17</span>
            </a>
          </li>
          <li class="page-menu-item">
            <a
              data-toggle="modal"
              data-target="#contact-form-modal"
              class="page-menu-link page-menu-link-button page-menu-link-button-black"
            >GET BASIC</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
    data() {
    return {
      notAtTop: false
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
      if (window.pageYOffset != 0) {
        this.notAtTop = true;
        console.log("heydo", this.notAtTop)
        return
      } else {
        this.notAtTop = false;
        console.log("deyho", this.notAtTop)
        return
      }
    }
  }
};
</script>


<style >

.navbar.page-menu {
    animation-duration: 1s;
    position: sticky;
    top: 42px;
    left: 0;
    z-index: 999;
    background: white;
    transition: all 0.25s ease-out;
}

.navbar.page-menu.not-at-top{
  box-shadow: 0 23px 47px -17px rgb(59 68 92 / 12%);
}

.navbar.page-menu.not-at-top .page-menu-wrapper{
  border: none;
}

.global-header.scrolled + .navbar.local-menu {
  top: 0;
}

.container {
  max-width: 1200px;
  width: 1170px;
  margin: 0 auto;
  position: relative;
  padding: 0 15px;
  box-sizing: border-box;
}

.page-menu-wrapper {
  padding-top: 25px;
  padding-bottom: 25px;
  border-bottom: 1px solid #fff;
  border-color: #32353d;
  width: 100%;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
  transition: border-color .2s ease-out;
height: 85px;
box-sizing: border-box;
}

.page-menu-logo {
  color: #1e1e1e;
  margin-right: 20px;
  display: block;
}

.page-menu-logo img {
    height: 30px;
    width: auto;
}

.page-menu-list {
  display: flex;
  align-items: center;
  justify-content: center;
}

.page-menu-item {
  margin-left: 22px;
  margin-right: 22px;
  background-color: transparent;
  display: inline-block;
  list-style: none;
  padding: 5px 10px 7px;
}

.page-menu-item:first-of-type {
  margin-left: 0;
}

.page-menu-item:last-of-type {
    padding-right: 0;
    margin-right: 0;
}

.page-menu-link {
  color: #32353d;
  position: relative;
  font-size: 15px;
  line-height: 18px;
      font-weight: 500;
      text-decoration: none;
}

.page-menu.transparent .page-menu-link-button {
    border: 2px solid #32353d;
    border-radius: 7px;
    font-weight: 700;
    text-transform: uppercase;
    color: #32353d;
    padding: 10px 25px;
    transition: all .3s ease-out;
    cursor: pointer;
}

.page-menu.transparent .page-menu-link-button:hover {
    box-shadow: 0 12px 26px -17px rgb(35 55 121 / 60%);
    background: #32353d;
    color: #fff!important;
}

.icon-count {
    position: absolute;
    top: -10px;
    right: -25px;
    width: 25px;
    height: 16px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    background: -webkit-gradient(linear,left bottom,left top,from(#ff002e),to(#ff002e)),-webkit-gradient(linear,left bottom,left top,from(#f09),to(#f09)),#71a4ff;
    background: linear-gradient(
0deg,#ff002e,#ff002e),linear-gradient(
0deg,#f09,#f09),#71a4ff;
    border-radius: 62px;
    -webkit-transform: rotate(
-21deg);
    transform: rotate(
-21deg);
    font-size: 12px;
    line-height: 14px;
    color: #fff;
}

</style>