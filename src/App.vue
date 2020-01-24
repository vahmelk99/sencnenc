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

      <Header :part="1" />
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

export default {
  name: "app",
  components: {
    Header,
    Middle,
    Footer
  },
  data() {
    return {
      partsLI: ["Profile", "Abilites", "Projects", "Experiences", "Contact"],
      showMenu: false,
      partColor: "white",
      footer: null,
      header: null,
      middle: {
        about: {
          heading: "About me",
          body: `Motivated young mathematician.\nCoding enthusiast and Data Science expert.\nLoving AI.`,
          details: {
            heading: "Details",
            body: {
              name: "Name",
              nameVal: "Zaven Badalyan",
              age: "Age",
              ageVal: 29,
              location: "Loaction",
              locationVal: "Berlin"
            }
          }
        },
        study: {
          heading: "Study",
          body: {
            bachelor: "Bachelor Degree",
            master: "Master Degree",
            masterMathBody:
              "In my Master Maths study I discovered the AI, especially deep learning. I used my Skills in the numerical Maths to understand Machine Learning and Deep Learning better. In my masters thesis I developed new type of AI algorithms. I finished the masters study in the year 2019 with the best mark.",
            phy: {
              heading: "in Physics",
              body:
                "Started to study physics at the Humbolst University of Berlin in year 2013. Wanted to be theoretica physicist. Physics teached me to look at things in a different way, from a new perpective."
            },
            math: {
              heading: "in Maths",
              body:
                "To be better theoretical physicist I started my Bachelor Maths in year 2014. Was specialized in numerical Maths and wrote mathematical simulation codes."
            }
          }
        },
        spec: {
          heading: "Specializations",
          body: {
            ai: {
              heading: "AI",
              body:
                "Felt in love with the AI after building my first face recognitial software. Was exited with the maths and the bilogical motivation behind of AI."
            },
            dataAnal: {
              heading: "Data Science and Analitics",
              body:
                "My mathematical skills made me an expert in Data Science. I always loved Statistics and Stochastcs. Combined with the AI it is the perfect mix to be a competent Data Scientist."
            },
            opt: {
              heading: "Optimization",
              body:
                "My Masters Maths gave me huge skillst in the area of Optimization. There I discovered that the deep understanindg of Mathematical Optimization helps you to understand the problematic of AI algorithms which are sometimes not sufficient good enough."
            },
            diff: {
              heading: "Differential Equations",
              body:
                "Differential Equations help us to model the reality. They require a huge expertise to choose the right DE to model in the reality. FEM is a discretization method to solve DE in the computer, this is a really difficult area and needs careflul expertise."
            }
          }
        },
        coding: {
          heading: "ALB"
        },
        project: {
          heading: "ALB"
        }
      }
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
