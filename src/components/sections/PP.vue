<template>
  <transition name="slide-fade">
    <div v-show="showSelf" class="con" @click.self="showSelf = false">
      <div class="inner">
        <div class="header">
          <h2>{{pp}}</h2>
          <span @click="showSelf = false" class="times">&times;</span>
        </div>
        <div class="body">{{val}}</div>
      </div>
    </div>
  </transition>
</template>

<script>
import Data from "./PPText";
export default {
  name: "PP",
  props: {
    text: String,
    show: Boolean
  },
  data() {
    return {
      val: "",
      pp: "",
      showSelf: false
    };
  },
  watch: {
    text() {
      this.pp = Data.header[this.$props.text];
      this.val = Data[this.text];
      console.log(this.text);
    },
    show() {
      this.showSelf = this.show;
    },
    showSelf() {
      if (!this.showSelf) {
        this.$emit("hide");
        document.body.style.overflowY = "scroll";
      } else document.body.style.overflow = "hidden";
    }
  }
};
</script>

<style scoped>
.body {
  margin-right: 25px;
  padding-right: 10px;
  overflow-y: scroll;
  max-height: 85vh;
  scrollbar-color: rgb(144, 203, 255) white;
  scrollbar-width: thin;
  white-space: pre-wrap;
}
.times {
  font-size: 35px;
  line-height: 16px;
  margin-right: 20px;
  color: black;
  padding: 5px;
}
.times:hover {
  color: rgb(144, 203, 255);
  cursor: pointer;
}
.header {
  /* padding-right: 30px; */
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 10px;
}
.inner {
  overflow: hidden;
  max-height: 90vh;
  background-color: white;
  padding: 25px 0px 30px 35px;
  border-radius: 10px;
  max-width: 1000px;
  width: 100%;
}
.con {
  background-color: rgba(95, 95, 95, 0.52);
  width: 100%;
  height: 100%;
  z-index: 500000;
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
}
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
</style>