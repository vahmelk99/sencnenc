<template>
  <div class="con" id="Experiences">
    <div class="head">
      <h1>Project Experience</h1>
      <img src="../../assets/man.png" />
    </div>
    <div class="inner">
      <img src="../../assets/man.png" />
      <div class="info">
        <div>
          <h2>Startselect</h2>
          <h2>Online Prepaid Services</h2>
          <p>Mart 2014 - May 2014</p>
          <h2>Course</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt ducimus, nisi optio voluptate dolorum impedit libero veniam? Eaque, culpa omnis illo, quidem quo unde, error asperiores necessitatibus quam id perspiciatis!</p>
        </div>
        <div class="third">
          <h2>Startselect</h2>
          <h2>Online Prepaid Services</h2>
          <p>Mart 2014 - May 2014</p>
          <h2>Course</h2>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt ducimus, nisi optio voluptate dolorum impedit libero veniam? Eaque, culpa omnis illo, quidem quo unde, error asperiores necessitatibus quam id perspiciatis!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience"
};
</script>

<style scoped>
.info > div:first-child {
  margin-bottom: 30px;
}
.con {
  padding: 85px 10vw;
  background-color: rgba(122, 118, 118, 0.1);
}
.inner > img {
  width: 250px;
  margin-right: 10vw;
  height: 100%;
}
.inner {
  display: flex;
  justify-content: center;
  text-align: right;
  margin-top: 50px;
}
.inner > div {
  width: 300px;
  padding-left: 30px;
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
    padding: 85px 30px;
  }
  .inner > div {
    width: 100%;
  }
}
</style>