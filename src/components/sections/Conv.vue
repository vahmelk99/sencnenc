<template>
  <form @submit="submit" class="conv">
    <input :value="email" type="email" :placeholder="pl1 + ' *'" />
    <textarea :value="message" :placeholder="pl2 + ' *'" cols="30" rows="10"></textarea>
    <input class="sub" type="submit" :value="subTxt" />
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: "Conv",
  data() {
    return {
      email: "",
      message: ""
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
      axios.post("http://badalyan.it:3000", {
        email: this.email,
        message: this.message
      });
      this.email = this.message = "";
    }
  }
};
</script>

<style scoped>
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
.sub:hover {
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
  border: 3px solid green;
  padding: 13px;
  width: 80%;
  border-radius: 5px;
}
.conv {
  padding: 93px 0 50px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.conv > *:focus {
  border-color: rgb(255, 2, 2) !important;
}
</style>