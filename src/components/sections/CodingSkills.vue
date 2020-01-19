<template>
  <div class="coding_skills_container">
    <h1>Coding Skills</h1>
    <div class="skills">
      <div class="python_card">
        <div class="python_heading">
          <div class="python_logo"></div>
          <div>Python</div>
        </div>
        <div class="python_stars">
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
        </div>
        <h4 class="ml_h">Machine Learning Libraries</h4>
        <div class="ml_h_libs">
          <div>
            <div class="tens_log"></div>
            <span>Tensorflow</span>
          </div>
          <div>
            <div class="pytorch_log"></div>
            <span>Pytorch</span>
          </div>
          <div>
            <div class="keras_log"></div>
            <span>Keras</span>
          </div>
        </div>
        <h4 class="stat_h">Statistics Libraries</h4>
        <div class="stat_h_libs">
          <div>
            <div class="pandas_log"></div>
            <span>Pandas</span>
          </div>
          <div>
            <div class="scikit_learn_log"></div>
            <span>Scikit-learn</span>
          </div>
        </div>
        <h4 class="math_h">Math Libraries</h4>
        <div class="math_h_libs">
          <div>
            <div class="numpy_log"></div>
            <span>Numpy</span>
          </div>
          <div>
            <div class="scipy_log"></div>
            <span>Scipy</span>
          </div>
          <div>
            <div class="dolphin_log"></div>
            <span>Dolphin-adjoint</span>
          </div>
        </div>
      </div>
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
.coding_skills_container {
  width: 70%;
  margin: 0 auto;
  margin-top: 50px;
  /* background-color: red; */
}
.coding_skills_container > h1:first-child {
  text-align: center;
}
.skills {
  width: 100%;
  background-color: rgba(122, 118, 118, 0.1);
  display: flex;
  justify-content: space-between;
}
.python_card {
  width: 30%;
  /* background-color: blue; */
}
.python_heading {
  display: flex;
  justify-content: center;
  height: 40px;
  font-size: 30px;
  font-weight: bold;
  line-height: 40px;
}
.python_card > h4 {
  /* text-align: center; */
  padding-left: 10%;
}
.python_stars {
  display: flex;
  width: 50%;
  justify-content: space-around;
  margin: 0 auto;
}
.star_filled {
  color: #f89621;
}
.ml_h,
.stat_h,
.math_h {
  margin-top: 10px;
  font-size: 17px;
}
.ml_h::before,
.stat_h::before,
.math_h::before {
  content: "\22B6     ";
}
.ml_h_libs,
.stat_h_libs,
.math_h_libs {
  /* background-color: red; */
  padding-left: 30%;
}
.tens_log,
.pytorch_log,
.keras_log,
.pandas_log,
.numpy_log,
.scipy_log,
.dolphin_log,
.scikit_learn_log {
  display: inline-block;
  width: 15px;
  height: 15px;
  border-radius: 15px;
  position: relative;
  top: 2px;
  margin-right: 5px;
  background-size: cover;
}
.python_logo {
  display: inline-block;
  width: 25px;
  height: 25px;
  border-radius: 15px;
  position: relative;
  top: 8px;
  margin-right: 3px;
  background-image: url("../../assets/little_icons/python.png");
  background-size: cover;
}
.tens_log {
  background-image: url("../../assets/little_icons/tensorflow.png");
}
.pytorch_log {
  background-position: -4px -2px;
  background-image: url("../../assets/little_icons/pytorch.png");
}
.keras_log {
  background-image: url("../../assets/little_icons/keras.jpg");
}
.pandas_log {
  background-image: url("../../assets/little_icons/pandas.png");
}
.numpy_log {
  background-image: url("../../assets/little_icons/numpy.png");
}
.scipy_log {
  background-image: url("../../assets/little_icons/scipy.png");
}
.dolphin_log {
  background-image: url("../../assets/little_icons/dolfinadjoint.png");
}
.scikit_learn_log {
  background-image: url("../../assets/little_icons/scikit-learn.png");
}
</style>