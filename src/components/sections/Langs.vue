<template>
  <div class="con" id="Languages">
    <section>
      <h1>{{langs.heading}}</h1>
      <div>
        <div>
          <div class="deu">
            <div class="photo">
              <img src="../../assets/langs/Deutsch.png" class="img" />
            </div>
            <div class="text">
              <h1>{{langs.de.heading}}</h1>
              <p>{{langs.de.body}}</p>
            </div>
          </div>

          <div class="en">
            <div class="photo">
              <img src="../../assets/langs/English.png" class="img" />
            </div>
            <div class="text">
              <h1>{{langs.en.heading}}</h1>
              <p>{{langs.en.body}}</p>
            </div>
          </div>
        </div>
        <div>
          <div class="ru">
            <div class="photo">
              <img src="../../assets/langs/Russian.png" class="img" />
            </div>
            <div class="text">
              <h1>{{langs.ru.heading}}</h1>
              <p>{{langs.ru.body}}</p>
            </div>
          </div>
          <div class="arm">
            <div class="photo">
              <img src="../../assets/langs/Armenian.png" class="img" />
            </div>
            <div class="text">
              <h1>{{langs.am.heading}}</h1>
              <p>{{langs.am.body}}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Langs",
  props: {
    langs: Object
  }
};
</script>

<style scoped>
section {
  /* width: 80%; */
  padding: 93px 15vw 40px 15vw;
  margin: 0 auto;
}
section > div {
  display: flex;
  justify-content: space-between;
}
section > div > div {
  flex: 1;
  display: flex;
  justify-content: space-between;
}
.con {
  background-color: #f1f1f1;
}
.text > h1 {
  margin-bottom: 20px;
}
section > h1 {
  text-align: center;
  font-size: 37px;
  padding-bottom: 40px;
}
section > div > div > div {
  display: flex;
  flex: 1;
  flex-direction: column;
  align-items: center;
  margin-bottom: 50px;
}
.text {
  width: 80%;
}
.img {
  width: 120px;
  transition: 1s ease;
}
.text > h1 {
  text-align: center;
}
@media screen and (max-width: 900px) {
  section > div > div > div {
    display: block;
    margin-bottom: 30px;
  }
  section > div > div > div > div {
    width: 70%;
    margin: 0 auto;
  }
  section {
    padding: 67px 5vw 40px 5vw;
  }
  .photo {
    display: flex;
    justify-content: center;
    flex-direction: row;
  }
}
@media screen and (max-width: 700px) {
  section > div {
    display: block;
  }
}
@media screen and (max-width: 444px) {
  section > div > div {
    display: block;
  }
}
</style>