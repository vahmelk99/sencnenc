<template>
  <div class="con">
    <h1>Specializations</h1>
    <div class="inner">
      <div>
        <img src="../../assets/nn.png" />
        <div>
          <h2>AI</h2>
        </div>
      </div>
      <div>
        <img src="../../assets/graphs.png" />
        <div>
          <h2>AI</h2>
        </div>
      </div>
      <div>
        <img src="../../assets/plot.png" />
        <div>
          <h2>AI</h2>
        </div>
      </div>
      <div>
        <img src="../../assets/diff.png" />
        <div>
          <h2>AI</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Special"
};
</script>

<style scoped>
.con {
  background-color: white;
  padding: 0 10vw;
}
.inner h2 {
  text-align: center;
}
.con > h1 {
  text-align: center;
}
.inner > div {
  margin: 50px 0;
  display: flex;
  justify-content: center;
}
.inner > div > img {
  flex: 3;
}
.inner > div > div {
  flex: 2;
}
.inner > div:nth-child(odd) {
  flex-direction: row-reverse;
}
</style>