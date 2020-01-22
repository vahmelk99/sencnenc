<template>
  <div class="about_sec_all" id="Profile">
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
  name: "AboutSection"
};
</script>
<style scoped>
.about_sec_all {
  padding-top: 87px;
  display: flex;
  justify-content: space-around;
  width: 80%;
  padding-right: 10%;
  padding-left: 10%;
  background-color: white;
}
.about_me {
  width: 30%;
}
.about_me > h1 {
  text-align: center;
  /* margin-top: 25px; */
}
.about_me > p {
  width: 80%;
  margin: 0 auto;
  text-align: center;
  margin-top: 25px;
}
.photo_cont {
  width: 30%;
  height: 400px;
  margin-top: 55px;
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
    margin-bottom: 50px;
  }
  .about_me {
    width: 100%;
  }
  .photo_cont {
    display: inline-flex;
    width: 50%;
    border-radius: 30px;
    border-bottom-left-radius: 150px;
    border-bottom-right-radius: 0px;
    background-color: rgba(122, 118, 118, 0.1);
  }
  .details_cont {
    height: auto;
    padding-bottom: 90px;
    width: 49%;
    border-radius: 30px;
    border-top-right-radius: 150px;
    border-top-left-radius: 0px;
    background-color: rgba(122, 118, 118, 0.1);
    display: inline-block;
  }
  .details_cont > h1 {
    margin-top: 90px;
  }
  .photo {
    margin-top: 35px;
  }
}
@media screen and (max-width: 800px) {
  .about_sec_all {
    flex-direction: column;
    align-items: center;
    width: 100%;
    padding-right: 0;
    margin-bottom: 0;
    padding-left: 0;
  }
  .about_sec_all > div {
    width: 100%;
  }
  .details_cont,
  .photo_cont {
    background-color: white;
  }
  .details_cont > h1 {
    margin-top: 0;
  }
}
</style>