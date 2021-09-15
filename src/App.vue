<template>
  <div id="app">
    <GlobalMenu></GlobalMenu>
    <HeaderMenu></HeaderMenu>
    <section class="first-section basic-section"></section>
    <section class="banner-section basic-section">
      <div class="banner-icons">
        <div id="left-1" class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="8.5s">
          <img src="./assets/svgs/messenger.svg" alt />
        </div>

        <div
          id="left-2"
          class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="9.1s"
        >
          <img src="./assets/svgs/design.svg" alt />
        </div>

        <div
          id="left-3"
          class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="8.8s"
        >
          <img src="./assets/svgs/payments.svg" alt />
        </div>

        <div
          id="left-4"
          class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="9.7s"
        >
          <img src="./assets/svgs/music.svg" alt />
        </div>

        <div
          id="left-5"
          class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="9.4s"
        >
          <img src="./assets/svgs/meetups.svg" alt />
        </div>

        <div
          id="left-6"
          class="banner-icon wow animate__slideInLeft"
          data-wow-duration="0.7s"
          data-wow-delay="10s"
        >
          <img src="./assets/svgs/moderation.svg" alt />
        </div>

        <div id="right-1" class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="8.5s">
          <img src="./assets/svgs/toolbox.svg" alt />
        </div>

        <div
          id="right-2"
          class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="9.1s"
        >
          <img src="./assets/svgs/referral.svg" alt />
        </div>

        <div
          id="right-3"
          class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="8.8s"
        >
          <img src="./assets/svgs/finances.svg" alt />
        </div>

        <div
          id="right-4"
          class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="9.7s"
        >
          <img src="./assets/svgs/hack.svg" alt />
        </div>

        <div
          id="right-5"
          class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="9.4s"
        >
          <img src="./assets/svgs/copyright.svg" alt />
        </div>

        <div
          id="right-6"
          class="banner-icon wow animate__slideInRight"
          data-wow-duration="0.7s"
          data-wow-delay="10s"
        >
          <img src="./assets/svgs/instagram.svg" alt />
        </div>
      </div>
      <div class="banner-content">
        <div class="banner-title wow fadeInUp">
          <div class="banner-left-text">Package</div>
          <span class="linear-wipe">Basic</span>
          <span class="sup-text wow opacity1"
              data-wow-duration="0.5s"
              data-wow-delay="3s"
              >
            <span
              class="number wow animate__fadeInLeft"
              data-wow-duration="1s"
              data-wow-delay="4s"
            >100%</span>
            <span
              class="wow animate__fadeInUp"
              data-wow-duration="1s"
              data-wow-delay="5s"
            >Must Have</span>
            <span
              class="wow animate__fadeInUp"
              data-wow-duration="1s"
              data-wow-delay="5.2s"
            >for YouTubers</span>
          </span>
          <div class="not-service not-service-desktop">
            <div
              class="not-service-icon wow pathToRight"
              data-wow-duration="1s"
              data-wow-delay="7.5s"
            ></div>
            <div class="not-service-text wow animate__fadeInUp"
              data-wow-duration="1s"
              data-wow-delay="6.2s"
              >Not provided by</div>
            <div class="not-service-adSense wow animate__fadeInUp"
              data-wow-duration="1s"
              data-wow-delay="6.5s"
              >AdSense</div>
          </div>
        </div>
        <div
          class="banner-desc wow animate__fadeInUp"
          data-wow-duration="1s"
          data-wow-delay="1s"
        >17 essential services to support, develop and</div>
        <div
          class="banner-desc wow animate__fadeInUp"
          data-wow-duration="1s"
          data-wow-delay="1.5s"
        >protect your creativity on YouTube and beyond</div>
        <div
          class="banner-desc-sub wow animate__fadeInUp"
          data-wow-duration="1s"
          data-wow-delay="2s"
        >Accessible immediately after connecting to AIR Creators Ecosystem.</div>
        <div
          class="banner-button wow animate__fadeInUp"
          data-wow-duration="1s"
          data-wow-delay="2.5s"
        >
          <a class="basic-button basic-button-big basic-button-blue">GET now</a>
        </div>
      </div>
    </section>
    <section class="single-text-sextion basic-section">
      <div class="moto-wrap wow animate__fadeInUp" data-wow-duration="1s" data-wow-delay="1s">
        <h3 class="moto">Don't sweat the minor staff, focus on what really matters!</h3>
      </div>
    </section>
  </div>
</template>

<script>
import HeaderMenu from "./components/HeaderMenu";
import GlobalMenu from "./components/GlobalMenu";

export default {
  name: "App",
  components: {
    HeaderMenu,
    GlobalMenu
  }
};
</script>

<style>
@import "./assets/fonts/Gilroy/gilroy.css";
/* @import "animate.css"; */

body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

* {
  animation-fill-mode: forwards;
}

a,
a:hover {
    text-decoration: none;
}

#app {
  position: relative;
  font-family: Gilroy, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.basic-section {
  height: 100vh;
}

.banner-section {
  position: relative;
}

.banner-icons {
  max-width: 1200px;
  width: 1170px;
  position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
  margin: 0 auto;
  box-sizing: border-box;
}

.banner-icon {
  position: absolute;
  width: 89px;
  height: 89px;
  border-radius: 20px;
  display: inline-block;
  opacity: 0;
  animation-fill-mode: forwards;
  animation-timing-function: ease-out;
}

.banner-icon img {
  width: 100%;
  height: 100%;
  -webkit-box-shadow: 7px 18px 16px rgb(0 0 0 / 20%);
  box-shadow: 7px 18px 16px rgb(0 0 0 / 20%);
  border-radius: 20px;
  -o-object-fit: contain;
  object-fit: contain;
}

#left-1 {
  top: 50px;
  left: 0;
}

#left-2 {
  top: 120px;
  left: -130px;
}

#left-3 {
  top: 215px;
  left: -10px;
}

#left-4 {
  top: 315px;
  left: -120px;
}

#left-5 {
  top: 404px;
  left: 10px;
}

#left-6 {
  top: 515px;
  left: -90px;
}

#right-1 {
  top: 50px;
  right: 0;
}

#right-2 {
  top: 120px;
  right: -130px;
}

#right-3 {
  top: 215px;
  right: -10px;
}

#right-4 {
  top: 315px;
  right: -120px;
}

#right-5 {
  top: 404px;
  right: 10px;
}

#right-6 {
  top: 515px;
  right: -90px;
}

#left-1 img {
  transform: rotate(-25deg);
}

#left-2 img {
  transform: rotate(-10deg);
}

#left-3 img {
  transform: rotate(20deg);
}

#left-4 img {
  transform: rotate(15deg);
}

#left-5 img {
  transform: rotate(22deg);
}

#left-6 img {
  transform: rotate(-5deg);
}

#right-1 img {
  transform: rotate(25deg);
}

#right-2 img {
  transform: rotate(10deg);
}

#right-3 img {
  transform: rotate(-20deg);
}

#right-4 img {
  transform: rotate(-15deg);
}

#right-5 img {
  transform: rotate(-22deg);
}

#right-6 img {
  transform: rotate(5deg);
}

.banner-content {
  padding: 100px 0;
  max-width: 700px;
  margin: 0 auto;
  text-align: center;
}

.banner-title {
  position: relative;
  font-size: 268px;
  line-height: 268px;
  animation: fadeInUp 1s;
}

.banner-title .banner-left-text {
  display: none;
  position: absolute;
  bottom: 15px;
  left: 0;
  -webkit-transform-origin: left;
  transform-origin: left;
  font-weight: 700;
  color: #39323e;
  text-transform: uppercase;
  -webkit-transform: rotate(-90deg);
  transform: rotate(-90deg);
  display: block;
  font-size: 42px;
  line-height: 52px;
}

.linear-wipe {
  background: -webkit-gradient(
    linear,
    left top,
    right top,
    color-stop(20%, #32353d),
    color-stop(40%, #1448ff),
    color-stop(60%, #1448ff),
    color-stop(80%, #32353d)
  );
  background: linear-gradient(
    90deg,
    #32353d 20%,
    #1448ff 40%,
    #1448ff 60%,
    #32353d 80%
  );
  background-size: 200% auto;
  color: #000;
  background-clip: text;
  text-fill-color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -webkit-animation: shine 2s linear infinite;
  animation: 2000ms linear 0ms infinite normal none running shine;
  font-size: 268px;
  line-height: 268px;
  font-weight: 700;
}

.not-service-desktop {
  display: block;
  position: relative;
}

.not-service-icon {
  position: absolute;
  top: -65px;
  left: -82px;
  width: 30.76px;
  height: 43.34px;
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: contain;
  background-image: url(./assets/images/arrow.png);
  clip-path: inset(0 100% 0 0);
}

.not-service-text {
  position: absolute;
  bottom: -15px;
  left: -130px;
  width: 90px;
  font-size: 12px;
  line-height: 19px;
  font-weight: 400;
  text-align: center;
  color: #b0b0b0;
  opacity: 0;
}

.not-service-adSense {
  position: absolute;
  bottom: -35px;
  left: -130px;
  width: 90px;
  font-size: 12px;
  line-height: 19px;
  font-weight: 400;
  text-align: center;
  color: #b0b0b0;
  opacity: 0;
}

.sup-text {
  top: 0;
  right: -110px;
  font-size: 12px;
  line-height: 14px;
  width: 135px;
  height: 135px;
  position: absolute;
  font-weight: 400;
  text-align: center;
  color: #b0b0b0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
  background-image: url(./assets/images/circle.png);
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: contain;
  opacity: 0;
}

.sup-text .number {
  font-size: 34px;
  line-height: 34px;
  font-weight: 700;
}

.sup-text span {
  opacity: 0
}

.banner-desc {
  font-size: 32px;
  line-height: 50px;
  font-style: normal;
  font-weight: 500;
  text-align: center;
  color: #484848;
  margin-bottom: 5px;
  opacity: 0;
}

.banner-desc-sub {
  font-size: 18px;
  line-height: 28px;
  margin-bottom: 40px;
  font-style: normal;
  font-weight: 400;
  color: #b0b0b0;
  opacity: 0;
  margin-top: 20px;
}

.banner-button {
  margin-bottom: 25px;
  opacity: 0;
}

.basic-button-blue {
  color: #f6f7fb;
  background: #1448ff;
  margin: 0 auto;
  font-size: 18px;
  line-height: 18px;
  height: 59px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  border-radius: 9px;
  font-weight: 500;
  width: 220px;
  padding: 20px 60px;
  box-shadow: 0 12px 26px -17px rgb(35 55 121 / 60%);
  transition: all .3s ease-out;
}

.basic-button-blue:hover {
    color: #f6f7fb;
    -webkit-box-shadow: 0 12px 26px -8px rgb(35 55 121 / 60%);
    box-shadow: 0 12px 26px -8px rgb(35 55 121 / 60%);
}

.single-text-sextion {
  display: flex;
  justify-content: center;
  align-items: center;
}

.moto-wrap {
  width: 1000px;
  margin: 0 auto;
  opacity: 0;
}

.moto {
  font-size: 74px;
  line-height: 84px;
  font-weight: 700;
}

.pathToRight {
  animation-name: pathToRight;
}

.opacity1 {
  animation-name: opacity1;
}

@keyframes shine {
  100% {
    background-position: -200%;
  }
}

@keyframes opacity1 {
  100% {
    opacity: 1;
  }
}

@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translate3d(0, 20%, 0);
  }
  100% {
    opacity: 1;
    transform: translateZ(0);
  }
}

@keyframes slideInRight {
  0% {
    opacity: 1;
    transform: translate3d(500%, 0, 0);
  }
  100% {
    opacity: 1;
    transform: translateZ(0);
  }
}

@keyframes slideInLeft {
  0% {
    opacity: 1;
    transform: translate3d(-500%, 0, 0);
  }
  100% {
    opacity: 1;
    transform: translateZ(0);
  }
}

@keyframes pathToRight {
  0% {
    clip-path: inset(0 100% 0 0);
  }
  100% {
    clip-path: inset(0 0 0 0);
  }
}
</style>
