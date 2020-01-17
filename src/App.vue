<template>
  <div id="app">
    <div class="con">
      <div class="bg"></div>
      <div class="filtrBlack"></div>
      <div class="inner">
        <div class="textes">
          <p>WELCOME</p>
          <p>
            I'm an
            <span>AI SPECIALIST</span>
          </p>
          <p>DEVELOPER PROGRAMMER BUISNESSMAN</p>
          <div class="icons">
            <span v-for="social in socials" :class="`fa fa-${social}`" :key="social"></span>
          </div>
        </div>
      </div>
    </div>
    <div class="parts">
      <p class="partsLI" v-for="(part, i) in partsLI" :key="i">{{part}}</p>
    </div>

    <div class="parts mini">
      <div class="hamburger">
        <font-awesome-icon
          :class="[!showMenu ? 'hamOpen' : '', 'ham']"
          icon="bars"
          size="2x"
          @click="showMenu = !showMenu"
        />
      </div>
      <div class="partInner" v-show="showMenu">
        <p class="partsLI" v-for="(part, i) in partsLI" :key="i">{{part}}</p>
      </div>
    </div>
    <div class="con">
      <div class="inner">
        <div class="textes">
          <div class="downdiv">
            <font-awesome-icon class="downicon" icon="angle-double-down" size="3x" />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
// import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    // Header,
    Footer
  },
  data() {
    return {
      partsLI: ["Profile", "Experiences", "Abilites", "Projects", "Contacr"],
      socials: ["facebook", "linkedin", "twitter", "instagram"],
      showMenu: false
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  user-select: none;
}
.fa-facebook:hover {
  color: #3b5998;
}
.fa-linkedin:hover {
  color: #007bb5;
}
.fa-twitter:hover {
  color: #55acee;
}
.fa-instagram:hover {
  color: #ea4c89;
}
.downdiv {
  height: 90px;
}
.downicon {
  cursor: pointer;
  animation: downanim 2s infinite;
}
.downicon:hover,
.partsLI:hover {
  color: #00aeff;
}
.parts {
  color: white;
  position: sticky;
  top: 0;
  padding: 35px 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.mini {
  display: none;
  /* position: relative; */
}
.partsLI {
  cursor: pointer;
  font-size: 20px;
  font-weight: 600;
  margin: 0 25px;
}
.icons {
  /* margin-bottom: 56px; */
}
.icons > span {
  cursor: pointer;
  font-size: 25px;
  margin: 0 10px;
}
.textes > p:first-child {
  font-size: 30px;
}
.textes > p:nth-child(2) {
  word-wrap: break-word;
  font-size: 60px;
  margin: 30px 0;
}
.textes > p:nth-child(3) {
  font-size: 20px;
  margin-bottom: 20px;
}
.textes > p > span {
  font-weight: bold;
}
.textes {
  position: static;
  padding-top: 80px;
}
.inner {
  width: 100%;
  text-align: center;
  color: white;
}
.filtrBlack {
  position: absolute;
  height: 800px;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: -100;
}
.bg {
  position: absolute;
  filter: blur(2px);
  background-image: url("./assets/HeaderBG.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  height: 800px;
  width: 100%;
  background-color: black;
  z-index: -200;
}
.con {
  width: 100%;
}
.ham {
  background-color: #3f5c86af;
  cursor: pointer;
  padding: 10px;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
.hamOpen {
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
}
.partInner {
  position: absolute;
  top: 87px;
  width: 100%;
}
.partInner > p {
  margin: 0;
  padding: 20px 20px;
  background-color: #3f5c86af;
}
.partInner > p:hover,
.ham:hover {
  background-color: #1a2636af;
}
@keyframes downanim {
  0% {
    margin-top: 0;
  }
  50% {
    margin-top: 20px;
  }
  100% {
    margin-top: 0;
  }
}
@media screen and (max-width: 800px) {
  .parts {
    display: none;
  }
  .mini {
    display: block;
  }
  .hamburger {
    display: flex;
    justify-content: end;
    margin-right: 30px;
  }
}
.slide-fade-enter-active {
}
.slide-fade-leave-active {
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
</style>
