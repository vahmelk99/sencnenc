<template>
  <div>
    <div class="con" v-if="!part">
      <div class="bg"></div>
      <div class="filtrBlack"></div>
      <div class="inner">
        <div class="textes">
          <p>{{header.welcome}}</p>
          <p>
            {{header.iam}}
            <span>{{header.aiSpec}}</span>
          </p>
          <p>{{header.more}}</p>
          <div class="icons">
            <a ref="facebook" target="_blank" href="https://www.facebook.com/zaven.badalyan"></a>
            <a
              ref="linkedin"
              target="_blank"
              href="https://www.linkedin.com/in/zaven-badalyan-b8aa21168"
            ></a>
            <span
              v-for="social in socials"
              :class="`fa fa-${social}`"
              :key="social"
              @click="open(social)"
            ></span>
          </div>
        </div>
      </div>
    </div>
    <div class="con" v-else>
      <div class="inner">
        <div class="downdiv">
          <font-awesome-icon @click="goToLets" class="downicon" icon="angle-double-down" size="3x" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    part: Number,
    header: Object
  },
  data() {
    return {
      socials: ["facebook", "linkedin"]
    };
  },
  methods: {
    goToLets() {
      this.$emit("goToLets");
    },
    open(who) {
      this.$refs[who].click();
    }
  }
};
</script>

<style scoped>
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
.downicon:hover {
  color: #00aeff;
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
  background-image: url("../assets/HeaderBG.jpg");
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
</style>
