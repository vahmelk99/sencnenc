<template>
  <div id="app">
    <Header :part="0" ref="topper" />

    <div :class="[partColor, 'parts']">
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

    <Header :part="1" />
    <Middle />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Middle from "./components/Middle.vue";

export default {
  name: "app",
  components: {
    Header,
    Middle,
    Footer
  },
  data() {
    return {
      partsLI: ["Profile", "Experiences", "Abilites", "Projects", "Contact"],
      showMenu: false,
      partColor: "white"
    };
  },
  methods: {
    handleScroll() {
      this.partColor = window.scrollY < 445 ? "white" : "black";
    }
  },
  created() {
    this.handleScroll();
    window.addEventListener("scroll", this.handleScroll);
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
  user-select: none;
}
.white {
  color: white;
}
.black {
  color: black;
  background-color: rgba(255, 255, 255, 0.5);
}
.partsLI:hover {
  color: #00aeff;
}
.parts {
  position: sticky;
  top: 0;
  padding: 35px 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.mini {
  color: white;
  display: none;
}
.partsLI {
  cursor: pointer;
  font-size: 20px;
  font-weight: 600;
  margin: 0 25px;
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
