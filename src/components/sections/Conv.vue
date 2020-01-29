<template>
  <form @submit="submit" class="conv">
    <input v-model="email" :class="colorInp" type="email" :placeholder="pl1 + ' *'" />
    <textarea
      v-model="message"
      :class="colorTxt"
      :placeholder="pl2 + ' *'"
      cols="30"
      rows="10"
      required
    ></textarea>
    <input class="sub" type="submit" :value="subTxt" />
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: "Conv",
  data() {
    return {
      email: "vahmelk99@gmail.com",
      message: "a",
      colorInp: "green",
      colorTxt: "green"
    };
  },
  props: {
    pl1: String,
    pl2: String,
    subTxt: String
  },
  methods: {
    submit(e) {
      e.preventDefault();
      // path
      let re = /[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,3}$/.test(this.email);
      if (re) {
        if (this.message) {
          axios.post("http://badalyan.it:3000/contact", {
            email: this.email,
            message: this.message
          });
          this.colorInp = this.colorTxt = "green";
          this.email = this.message = "";
        } else this.colorTxt = "red";
      } else this.colorInp = "red";
    }
  }
};
</script>

<style scoped>
.red {
  border: 3px solid red;
}
.sub {
  background-color: green;
  border: none;
  padding: 13px 70px;
  font-size: 20px;
  color: white;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 70px;
}
.sub:hover,
.sub:focus {
  background-color: rgb(0, 93, 0);
}
.sub::-moz-focus-inner {
  border: 0;
}
.sub:visited {
  text-decoration: none;
}
.conv > input[type="email"] {
  max-width: 300px;
}
.conv > textarea {
  margin: 30px 0;
  resize: none;
  max-width: 500px;
}
.conv > input[type="email"],
.conv > textarea {
  padding: 13px;
  width: 80%;
  border-radius: 5px;
}
.green {
  border: 3px solid green;
}
.conv {
  padding: 93px 0 50px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.conv > *:focus {
  border-color: rgb(144, 203, 255) !important;
}
.conv > * {
  box-shadow: none !important;
}
</style>