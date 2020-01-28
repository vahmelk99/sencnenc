<template>
  <div id="app">
    <div>
      <Header :header="header" :part="0" ref="topper" />

      <div :class="[partColor, 'parts']">
        <p class="partsLI" v-for="(part, i) in partsLI" :key="i" @click="scrollTo(part)">{{part}}</p>
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
          <p
            class="partsLI"
            v-for="(part, i) in partsLI"
            :key="i"
            @click="scrollTo(part); showMenu = false"
          >{{part}}</p>
        </div>
      </div>

      <Header @goToLets="scrollTo('Lets')" :part="1" />
      <Middle :middle="middle" />
    </div>

    <Footer :footer="footer" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Middle from "./components/Middle.vue";
import { scroller } from "vue-scrollto/src/scrollTo";
const scroll = scroller();
import Data from "./components/Data.js";
export default {
  name: "app",
  components: {
    Header,
    Middle,
    Footer
  },
  data() {
    return {
      partsLI: [
        "Profile",
        "Study",
        "Specs",
        "Coding",
        "Languages",
        "Projects",
        "Science",
        "Contact"
      ],
      showMenu: false,
      partColor: "white",
      footer: Data.footer,
      header: Data.header,
      middle: Data.middle
    };
  },
  methods: {
    handleScroll() {
      this.partColor = window.scrollY < 445 ? "white" : "black";
    },
    scrollTo(el) {
      scroll(`#${el}`);
    }
  },

  created() {
    this.handleScroll();
    window.addEventListener("scroll", this.handleScroll);
    //request
    //
    //
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  /* user-select: none; */
}
.bold {
  font-weight: bold;
}
.white {
  color: white;
}
.black {
  color: black;
  background-color: rgba(255, 255, 255, 0.616);
}
.partsLI:hover {
  color: #00aeff;
}
.parts {
  z-index: 2;
  position: sticky;
  top: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.mini {
  color: white;
  display: none;
  padding: 35px 0;
}
.partsLI {
  cursor: pointer;
  padding: 35px 25px;
  font-size: 20px;
  font-weight: 600;
}
@media screen and (max-width: 985px) {
  .parts {
    display: none;
  }
  .mini {
    display: block;
  }
  .hamburger {
    display: flex;
    justify-content: flex-end;
    margin-right: 30px;
  }
}
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
.partInner > p:hover,
.ham:hover {
  background-color: #1a2636af;
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
</style>
