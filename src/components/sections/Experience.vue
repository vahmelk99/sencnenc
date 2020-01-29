<template>
  <div class="con" id="Projects">
    <div class="head">
      <h1>{{project.exp.heading}}</h1>
      <img src="../../assets/man.png" />
    </div>
    <div class="inner">
      <div class="info">
        <div>
          <p>{{project.exp.body}}</p>
        </div>
      </div>
      <img src="../../assets/man.png" />
    </div>
    <div class="head" id="Science">
      <h1>{{project.career.heading}}</h1>
      <img src="../../assets/Uxex.png" />
    </div>
    <div class="inner">
      <img src="../../assets/Uxex.png" />
      <div class="info">
        <div>
          <p>{{project.career.body}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",
  props: {
    project: Object
  }
};
</script>

<style scoped>
.info > div:first-child {
  margin-bottom: 30px;
}
#Science {
  padding-top: 93px;
}
.con {
  padding: 93px 10vw 50px 10vw;
  background-color: white;
}
.inner > img {
  width: 250px;
  margin: 0 10vw;
  height: 100%;
}
.inner {
  display: flex;
  justify-content: center;
  text-align: right;
  margin-top: 50px;
}
.inner > div:first-child {
  text-align: left;
}
.inner > div {
  width: 600px;
  padding: 0 30px;
}
.head > img {
  display: none;
  width: 50px;
  height: 100%;
  margin-left: 10px;
}
.head > h1 {
  text-align: center;
  margin-right: 10px;
}
@media screen and (max-width: 1000px) {
  .inner > img {
    margin: 0 5vw;
  }
}
@media screen and (max-width: 620px) {
  .head {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .inner > img {
    display: none;
  }
  .inner {
    text-align: center;
  }
  .head > img {
    display: block;
  }
  .con {
    padding: 93px 5vw 50px 5vw;
  }
  .inner > div {
    width: 100%;
  }
}
</style>