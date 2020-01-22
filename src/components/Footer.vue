<template>
  <div class="con">
    <div class="top">
      <div class="first">
        <h1>Immpresum</h1>
        <p>Zaven Badalyan</p>
        <p>Landsberger Allee 273</p>
        <p>13055 Berlin</p>
        <p>Germany</p>
      </div>
      <div class="sec">
        <h1>Connect</h1>
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
      <div class="third">
        <h1>Contact Me</h1>
        <input type="email" placeholder="Your Email" />
        <textarea placeholder="Message..."></textarea>
        <div class="send">Send</div>
      </div>
    </div>
    <div class="bot">
      <div class="pp">
        <h3>Pivacy Policy</h3>
        <span>EN</span>
        <span>DE</span>
      </div>
      <div class="copyr">
        <h3>&copy; Zaven Badalyan 2020</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>
.copyr {
  flex: 2;
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
.third > textarea,
.third > input {
  width: 97%;
  border: 1px solid rgb(90, 90, 90);
  border-radius: 5px;
  padding: 10px 1%;
}
.third > textarea:focus,
.third > input:focus {
  border-color: rgb(92, 179, 255);
}
.third > textarea::placeholder,
.third > input::placeholder {
  line-height: 16px;
  font-size: 10px;
  color: black !important;
}
.third > input {
  margin-bottom: 10px;
}
.third > textarea {
  height: 73px;
  resize: none;
  margin-bottom: 7px;
}
.third {
  flex: 1;
}
.third > h1 {
  text-align: center;
}

.top,
.bot {
  display: flex;
  padding: 0 15vw;
  flex-wrap: wrap;
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
.top > div,
.bot {
  padding-top: 20px;
  padding-bottom: 20px;
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
.third {
  max-width: 500px;
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
  .third {
    max-width: none;
  }
  .top {
    display: block;
  }
  .top > div:not(.third) {
    display: inline-block;
    width: 42%;
    padding: 20px 2%;
    vertical-align: top;
  }
}
@media screen and (max-width: 606px) {
  .top > div:not(.third) {
    display: block;
    width: 100%;
  }
  .bot {
    display: block;
  }
  .pp {
    margin-bottom: 20px;
  }
}
</style>
