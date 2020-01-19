<template>
  <div class="con">
    <div class="head">
      <img src="../../assets/glxark.png" />
      <h1>Study</h1>
    </div>
    <div class="secs">
      <img src="../../assets/react.png" />
      <div>
        <h2>Bachelor Degree</h2>
        <h3 class="bold">in Physics</h3>
        <p class="txt">
          <span class="bold">Lorem ipsum dolor sit amet consectetur,</span> adipisicing elit. Commodi ducimus incidunt enim assumenda nisi deleniti quam eligendi maxime at sed nostrum est odit neque hic dolore accusamus, odio voluptate aliquid. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Asperiores doloribus, enim accusantium corrupti inventore amet! Exercitationem dolorem aspernatur non saepe adipisci temporibus culpa, voluptas dicta, consequatur facere quasi laborum deserunt.
        </p>
      </div>
    </div>
    <div class="secs">
      <div>
        <h2>Bachelor Degree</h2>
        <h3 class="bold">in Maths</h3>
        <p
          class="txt"
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi ducimus incidunt enim assumenda nisi deleniti quam eligendi maxime at sed nostrum est odit neque hic dolore accusamus, odio voluptate aliquid. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Asperiores doloribus, enim accusantium corrupti inventore amet! Exercitationem dolorem aspernatur non saepe adipisci temporibus culpa, voluptas dicta, consequatur facere quasi laborum deserunt.</p>
      </div>
      <img src="../../assets/pi.png" />
    </div>
    <div class="secs">
      <img src="../../assets/pitag.png" />
      <div>
        <h2>Maste Degree</h2>
        <h3 class="bold">in Maths</h3>
        <p
          class="txt"
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi ducimus incidunt enim assumenda nisi deleniti quam eligendi maxime at sed nostrum est odit neque hic dolore accusamus, odio voluptate aliquid. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Asperiores doloribus, enim accusantium corrupti inventore amet! Exercitationem dolorem aspernatur non saepe adipisci temporibus culpa, voluptas dicta, consequatur facere quasi laborum deserunt.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Study"
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