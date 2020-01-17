<template>
  <div class="about_sec_all">
    <div class="about_me">
      <h1>About me</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae in illum, labore autem fugit cum corrupti impedit, id ex minima totam suscipit error voluptates tempore sequi pariatur architecto, quo iste? Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam minima, esse doloremque non fugit labore minus quod consectetur aspernatur sit libero error, veritatis ex. Amet nesciunt repellat sunt id cumque?</p>
    </div>
    <div class="photo_cont">
      <div class="photo"></div>
    </div>
    <div class="details_cont">
      <h1>Details</h1>
      <h4 class="name">Name</h4>
      <p>Zaven Badalyan</p>
      <h4 class="age">Age</h4>
      <p>XX</p>
      <h4 class="location">Location</h4>
      <p>XXXXXX</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  }
};
</script>
<style scoped>
.about_sec_all {
  padding-top: 100px;
  display: flex;
  justify-content: space-around;
  width: 80%;
  padding-right: 10%;
  padding-left: 10%;
  background-color: white;
}
.about_me {
  width: 30%;
  height: 400px;

  /* background-color: lightblue; */
}
.about_me > h1 {
  text-align: center;
  margin-top: 25px;
}
.about_me > p {
  width: 80%;
  margin: 0 auto;
  text-align: center;
  margin-top: 25px;
}
.photo_cont {
  width: 30%;
  /* background-color: lightblue; */
  height: 400px;

  display: flex;
  flex-direction: column;
  justify-content: center;
}
.photo {
  width: 300px;
  margin: 0 auto;
  height: 300px;
  border-radius: 100%;
  background-image: url("../../assets/profPic.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
.details_cont {
  width: 25%;
  /* background-color: lightblue; */
  height: 400px;
}

.details_cont > h1 {
  margin-top: 25px;
  text-align: center;
}
.details_cont > .name {
  margin-top: 35px;
  text-align: center;
}
.details_cont > p {
  margin-top: 5px;
  text-align: center;
}
.details_cont > .age,
.details_cont > .location {
  margin-top: 10px;
  text-align: center;
}
@media screen and (max-width: 1024px) {
  .about_sec_all {
    display: block;
  }
  .about_me {
    width: 100%;
    height: 200px;
  }
  .photo_cont {
    display: inline-flex;
    width: 49%;
    border-radius: 30px;
    border-bottom-left-radius: 150px;
    border-bottom-right-radius: 0px;
    background-color: rgba(122, 118, 118, 0.1);
  }
  .details_cont {
    width: 49%;
    border-radius: 30px;
    border-top-right-radius: 150px;
    border-top-left-radius: 0px;
    background-color: rgba(122, 118, 118, 0.1);
    display: inline-block;
  }
  .details_cont > h1 {
    margin-top: 60px;
  }
}
@media screen and (max-width: 800px) {
  .about_sec_all {
    padding-top: 50px;
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding-right: 0;
    padding-left: 0;
  }
  .about_me {
    height: 350px;
  }
  .about_sec_all > div {
    width: 100%;
  }
  .photo {
    margin-top: 25px;
  }
  .details_cont {
    background-color: white;
  }
  .photo_cont {
    background-color: white;
    height: 300px;
  }
}
</style>