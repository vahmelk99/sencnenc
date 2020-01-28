<template>
  <div class="con" id="Specs">
    <h1>{{spec.heading}}</h1>
    <div class="inner">
      <div>
        <div>
          <img src="../../assets/nn.png" />
        </div>
        <div>
          <h2>{{spec.body.ai.heading}}</h2>
          <p>{{spec.body.ai.body}}</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/graphs.png" />
        </div>
        <div>
          <h2>{{spec.body.dataAnal.heading}}</h2>
          <p>{{spec.body.dataAnal.body}}</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/plot.png" />
        </div>
        <div>
          <h2>{{spec.body.opt.heading}}</h2>
          <p>{{spec.body.opt.body}}</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/diff.png" />
        </div>
        <div>
          <h2>{{spec.body.diff.heading}}</h2>
          <p>{{spec.body.diff.body}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Special",
  props: {
    spec: Object
  }
};
</script>

<style scoped>
.con {
  background-color: #f1f1f1;
  padding: 93px 15vw;
}
.inner h2 {
  text-align: center;
}
.inner p {
  padding: 25px 50px;
}
.con > h1 {
  text-align: center;
}
.inner > div {
  margin-top: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.inner > div > div > img {
  width: 100%;
  transition: 1s ease;
  height: auto;
}
.inner > div > div:first-child {
  flex: 7;
}
.inner > div > div {
  flex: 6;
}
.inner > div:nth-child(odd) {
  flex-direction: row-reverse;
}
@media screen and (max-width: 1100px) {
  .inner > div,
  .inner > div:nth-child(odd) {
    display: flex;
    flex-direction: column-reverse;
  }
  .inner p {
    padding: 10px 0;
  }
  .inner > div > div > img {
    width: 50%;
  }
  .inner > div > div:first-child {
    display: flex;
    justify-content: center;
  }
}
@media screen and (max-width: 494px) {
  .inner > div > div > img {
    width: 100%;
  }
}
</style>