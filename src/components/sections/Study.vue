<template>
  <div class="con">
    <div class="head">
      <img src="../../assets/glxark.png" />
      <h1>{{study.heading}}</h1>
    </div>
    <div class="secs">
      <img src="../../assets/react.png" />
      <div>
        <h2>{{study.body.bachelor}}</h2>
        <h3 class="bold">{{study.body.phy.heading}}</h3>
        <p class="txt">{{study.body.phy.body}}</p>
      </div>
    </div>
    <div class="secs">
      <div>
        <h2>{{study.body.bachelor}}</h2>
        <h3 class="bold">{{study.body.math.heading}}</h3>
        <p class="txt">{{study.body.math.body}}</p>
      </div>
      <img src="../../assets/pi.png" />
    </div>
    <div class="secs">
      <img src="../../assets/pitag.png" />
      <div>
        <h2>{{study.body.master}}</h2>
        <h3 class="bold">{{study.body.math.heading}}</h3>
        <p class="txt">{{study.body.masterMathBody}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Study",
  props: {
    study: Object
  }
};
</script>
<style scoped>
.txt {
  text-align: left;
  margin-top: 10px;
  /* padding: 0 10vw; */
}
.secs > div {
  width: 50vw;
  /* flex: 1; */
  text-align: center;
  padding: 0 30px;
}
.secs {
  padding: 30px 10vw;
  display: flex;
  justify-content: center;
}
.secs > img {
  transition: 1s ease;
  width: 200px;
  height: 200px;
}
.head > img {
  width: 100px;
  height: auto;
  margin-right: 15px;
}
.head > h1 {
  margin-left: 15px;
}
.head {
  display: flex;
  justify-content: center;
  align-items: center;
}
.con {
  background-color: white;
}
@media screen and (max-width: 600px) {
  .secs > img {
    width: 50px;
    height: 50px;
  }
  .secs > div {
    padding: 0;
  }
}
</style>