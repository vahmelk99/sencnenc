<template>
  <div class="con" id="Abilites">
    <h1>Specializations</h1>
    <div class="inner">
      <div>
        <div>
          <img src="../../assets/nn.png" />
        </div>
        <div>
          <h2>AI</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima provident officiis doloribus sunt natus necessitatibus in consequatur porro ipsam sed a soluta et consectetur, deleniti vitae, enim obcaecati ab omnis?Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque nesciunt aspernatur assumenda, voluptatum dolorum aut necessitatibus omnis minus fugit perspiciatis adipisci maxime, eveniet praesentium harum ipsum expedita modi velit illum!</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/graphs.png" />
        </div>
        <div>
          <h2>Data Since and Analitics</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima provident officiis doloribus sunt natus necessitatibus in consequatur porro ipsam sed a soluta et consectetur, deleniti vitae, enim obcaecati ab omnis?Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque nesciunt aspernatur assumenda, voluptatum dolorum aut necessitatibus omnis minus fugit perspiciatis adipisci maxime, eveniet praesentium harum ipsum expedita modi velit illum!</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/plot.png" />
        </div>
        <div>
          <h2>Optimization</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima provident officiis doloribus sunt natus necessitatibus in consequatur porro ipsam sed a soluta et consectetur, deleniti vitae, enim obcaecati ab omnis?Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque nesciunt aspernatur assumenda, voluptatum dolorum aut necessitatibus omnis minus fugit perspiciatis adipisci maxime, eveniet praesentium harum ipsum expedita modi velit illum!</p>
        </div>
      </div>
      <div>
        <div>
          <img src="../../assets/diff.png" />
        </div>
        <div>
          <h2>Differential Equations</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minima provident officiis doloribus sunt natus necessitatibus in consequatur porro ipsam sed a soluta et consectetur, deleniti vitae, enim obcaecati ab omnis?Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque nesciunt aspernatur assumenda, voluptatum dolorum aut necessitatibus omnis minus fugit perspiciatis adipisci maxime, eveniet praesentium harum ipsum expedita modi velit illum!</p>
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
  padding: 0 15vw;
  padding-top: 87px;
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
  margin: 50px 0;
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