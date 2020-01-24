<template>
  <section>
    <h1>Languages</h1>
    <div class="deu">
      <div class="photo">
        <img src="../../assets/langs/Deutsch.png" class="img" />
      </div>
      <div class="text">
        <h1>Deutsch</h1>
        <h4>(National)</h4>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis officia explicabo harum neque, nostrum aspernatur ipsum vitae reiciendis beatae. A vitae ipsa optio libero amet voluptatibus. Nisi ab in amet.</p>
      </div>
    </div>
    <div class="en">
      <div class="photo">
        <img src="../../assets/langs/English.png" class="img" />
      </div>
      <div class="text">
        <h1>English</h1>
        <h4>(National)</h4>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis officia explicabo harum neque, nostrum aspernatur ipsum vitae reiciendis beatae. A vitae ipsa optio libero amet voluptatibus. Nisi ab in amet.</p>
      </div>
    </div>
    <div class="arm">
      <div class="photo">
        <img src="../../assets/langs/Armenian.png" class="img" />
      </div>
      <div class="text">
        <h1>Armenian</h1>
        <h4>(National)</h4>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis officia explicabo harum neque, nostrum aspernatur ipsum vitae reiciendis beatae. A vitae ipsa optio libero amet voluptatibus. Nisi ab in amet.</p>
      </div>
    </div>
    <div class="ru">
      <div class="photo">
        <img src="../../assets/langs/Russian.png" class="img" />
      </div>
      <div class="text">
        <h1>Russian</h1>
        <h4>(National)</h4>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis officia explicabo harum neque, nostrum aspernatur ipsum vitae reiciendis beatae. A vitae ipsa optio libero amet voluptatibus. Nisi ab in amet.</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Langs"
};
</script>

<style scoped>
section {
  width: 70%;
  padding: 67px 0px 40px 0px;
  margin: 0 auto;
  margin-bottom: 87px;
  background-color: rgba(122, 118, 118, 0.1);
}
section > div:nth-child(odd) {
  flex-direction: row-reverse;
}
section > h1 {
  text-align: center;
  font-size: 37px;
  margin-bottom: 40px;
}
section > div {
  display: flex;
  justify-content: space-around;
  margin-bottom: 50px;
  padding: 0 8%;
}
.text {
  width: 55%;
}
.photo {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.img {
  width: 120px;
}
.text > * {
  text-align: center;
}
@media screen and (max-width: 800px) {
  section > div {
    display: block;
    margin-bottom: 30px;
  }
  section > div > div {
    width: 70%;
    margin: 0 auto;
  }
  .text {
    width: 70%;
  }
  .photo {
    display: flex;
    justify-content: center;
    flex-direction: row;
  }
}
@media screen and (max-width: 560px) {
  .text {
    width: 70%;
  }
  section > div {
    margin-bottom: 20px;
  }
}
</style>