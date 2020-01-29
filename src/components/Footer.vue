<template>
  <div class="con" id="Contact">
    <div class="top">
      <div class="first">
        <h1>{{footer.immpresum}}</h1>
        <p>Zaven Badalyan</p>
        <p>Landsberger Allee 273</p>
        <p>13055 Berlin</p>
        <p>Germany</p>
      </div>
      <div class="sec">
        <h1>{{footer.connect}}</h1>
        <p>
          <span class="fa fa-facebook">Facebook</span>
        </p>
        <p>
          <span class="fa fa-linkedin">Linked In</span>
        </p>
        <p>
          <span class="fa fa-envelope">zaven@badalyan.it</span>
        </p>
        <p>
          <span class="fa fa-phone">+4901628344423</span>
        </p>
      </div>
    </div>
    <div class="bot">
      <div class="copyr">
        <h3>&copy; Zaven Badalyan 2020</h3>
      </div>
      <div class="pp">
        <h3>{{footer.pp}}</h3>
        <span>EN</span>
        <span>DE</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: {
    footer: Object
  }
};
</script>

<style scoped>
.copyr {
  flex: 2;
}
.pp > h3 {
  display: inline-block;
  margin: 10px 10px 0 10px;
}
.pp {
  flex: 1;
}
.send:hover,
.sec span:hover {
  cursor: pointer;
}
.sec span:hover {
  color: rgb(144, 203, 255);
}
.send:hover {
  background-color: rgb(182, 182, 182);
}
.send {
  padding: 5px 0;
  color: black;
  border-radius: 25px;
  font-size: 15px;
  width: 80px;
  text-align: center;
  background-color: white;
  display: inline-block;
}
.bot {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.top {
  display: flex;
  padding: 0 15vw;
  max-width: 800px;
  flex-wrap: wrap;
  margin: 0 auto;
  justify-content: space-between;
}
.con {
  overflow: hidden;
  color: white;
  background-color: rgb(61, 61, 61);
}
.con span,
.con p {
  font-size: 19px;
}
.top > div {
  padding-top: 40px;
}
.bot {
  padding: 20px 0;
}
.top > div > h1 {
  margin-bottom: 10px;
}
.sec span {
  padding: 10px 0;
}
.sec span::before {
  padding-right: 10px;
}
.sec {
  padding-left: 20px;
  padding-right: 20px;
}
.bot span {
  font-size: 15px;
  margin-right: 5px;
}
.bot span:hover {
  text-decoration: underline;
  cursor: pointer;
}
@media screen and (max-width: 885px) {
  .top {
    display: block;
  }
  .top > div {
    display: inline-block;
    width: 42%;
    padding: 20px 2%;
    vertical-align: top;
  }
}
@media screen and (max-width: 606px) {
  .top > div {
    display: block;
    width: 100%;
  }
  .bot {
    display: block;
  }
  .bot {
    margin-bottom: 20px;
    padding: 20px 15vw;
  }
}
</style>
