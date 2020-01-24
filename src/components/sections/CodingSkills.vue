<template>
  <div class="coding_skills_container">
    <h1>{{coding.heading}}</h1>
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
      <div class="r_card">
        <div class="r_heading">
          <div class="r_logo bold">R</div>
        </div>
        <div class="r_stars">
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
        </div>
        <h4 class="anal_h">Analyse & Explore</h4>
        <div class="anal_h_libs">
          <div>
            <div class="tidyverse_logo"></div>
            <span>Tidyverse</span>
          </div>
          <div>
            <div class="ggplot_logo"></div>
            <span>Ggplot 2</span>
          </div>
          <div>
            <div class="dplyr_logo"></div>
            <span>Dplyr</span>
          </div>
          <div>
            <div class="tidyr_logo"></div>
            <span>Tidyr</span>
          </div>
          <div>
            <div class="purrr_logo"></div>
            <span>Purrr</span>
          </div>
        </div>
        <h4 class="model_h">Model & Predict</h4>
        <div class="model_h_libs">
          <div>
            <div class="tensorflow_logo"></div>
            <span>TensorFlow</span>
          </div>
          <div>
            <div class="tidymodels_logo"></div>
            <span>Tidymodels</span>
          </div>
          <div>
            <div class="sparklyr_logo"></div>
            <span>Sparklyr</span>
          </div>
          <div>
            <div class="stringr_logo"></div>
            <span>Stringr</span>
          </div>
        </div>
      </div>
      <div class="matlab_card">
        <div class="matlab_heading">
          <div class="matlab_logo"></div>
          <div>MatLab</div>
        </div>
        <div class="matlab_stars">
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
        </div>
        <h4 class="stat_tool_h">Statistics Toolbox</h4>
        <h4 class="machin_h">Machine Learning Toolbox</h4>
        <h4 class="optim_h">Optimization Toolbox</h4>
        <h4 class="curve_h">Curve Fitting Toolbox</h4>
        <h4 class="diff_h">Differential Equation Toolbox</h4>
      </div>
    </div>
    <div class="skills">
      <div class="latex_card">
        <div class="latex_heading">
          <div class="latex_logo"></div>
          <div>Latex</div>
        </div>
        <div class="latex_stars">
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
        </div>
        <h4 class="beamer_h">Beamer</h4>
        <h4 class="pgf_h">PGF/TikZ</h4>
        <div class="ms_heading">
          <div class="ms_logo"></div>
          <div>MS Office</div>
        </div>
        <div class="ms_stars">
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
          <font-awesome-icon class="star_filled" icon="star" />
        </div>
        <h4>Word</h4>
        <h4>Excel</h4>
        <h4>Powerpoint</h4>
      </div>
      <div class="other_card">
        <div class="other_heading">{{coding.body.other.heading}}</div>
        <div class="other_row">
          <h4 v-for="(code, index) in coding.body.other.body" :key="index">{{code}}</h4>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "CodingSkills",
  props: {
    coding: Object
  }
};
</script>
<style scoped>
.coding_skills_container {
  width: 70%;
  margin: 0 auto;
  background-color: white;
  padding-bottom: 50px;
}
.coding_skills_container > h1:first-child {
  text-align: center;
  margin-bottom: 10px;
}
.skills {
  width: 100%;
  /* background-color: red; */
  display: flex;
  justify-content: space-between;
}
.skills:nth-of-type(2) {
  margin-top: 20px;
  justify-content: space-around;
}
.skills > div {
  padding: 10px 0px;
}
.python_card,
.matlab_card,
.r_card,
.latex_card,
.other_card {
  width: 30%;
  background-color: rgba(122, 118, 118, 0.1);
  /* background-color: blue; */
}
.python_heading,
.matlab_heading,
.latex_heading,
.r_heading,
.ms_heading,
.other_heading {
  display: flex;
  justify-content: center;
  height: 40px;
  font-size: 30px;
  font-weight: bold;
  line-height: 40px;
}
.python_card > h4,
.matlab_card > h4,
.r_card > h4,
.latex_card > h4,
.other_card h4 {
  /* text-align: center; */
  padding-left: 10%;
}
.matlab_card > h4 {
  margin-bottom: 10px;
  font-size: 17px;
}
.python_stars,
.matlab_stars,
.latex_stars,
.r_stars,
.ms_stars {
  display: flex;
  width: 50%;
  justify-content: space-around;
  margin: 0 auto;
  margin-top: 5px;
  margin-bottom: 5px;
}
.star_filled {
  color: #f89621;
}
.ml_h,
.stat_h,
.math_h,
.anal_h,
.model_h {
  /* margin-top: 10px; */
  font-size: 17px;
}
.ml_h::before,
.stat_h::before,
.machin_h::before,
.math_h::before,
.stat_tool_h::before,
.optim_h::before,
.curve_h::before,
.diff_h::before,
.part_diff_h::before,
.beamer_h::before,
.pgf_h::before,
.anal_h::before,
.model_h::before,
.ms_heading ~ h4::before,
.other_row h4::before {
  content: "\22B6     ";
  color: #f89621;
}
.other_heading ~ h4 {
  margin-bottom: 5px;
}
.ml_h_libs,
.stat_h_libs,
.math_h_libs,
.anal_h_libs,
.model_h_libs {
  padding-left: 30%;
}
.tens_log,
.pytorch_log,
.keras_log,
.pandas_log,
.numpy_log,
.scipy_log,
.dolphin_log,
.scikit_learn_log,
.tidyverse_logo,
.ggplot_logo,
.dplyr_logo,
.tidyr_logo,
.purrr_logo,
.tensorflow_logo,
.tidymodels_logo,
.sparklyr_logo,
.stringr_logo {
  background-repeat: no-repeat;
  display: inline-block;
  width: 15px;
  height: 15px;
  border-radius: 15px;
  position: relative;
  top: 2px;
  margin-right: 5px;
  background-size: cover;
}
.python_logo,
.matlab_logo,
.r_logo,
.latex_logo,
.ms_logo {
  display: inline-block;
  width: 25px;
  height: 25px;
  border-radius: 15px;
  position: relative;
  top: 8px;
  margin-right: 3px;
  background-size: cover;
}
/* .r_logo { */
/* background-image: url("../../assets/little_icons/r.jpg"); */
/* } */
.latex_logo {
  background-image: url("../../assets/little_icons/latex.png");
}
.ms_logo {
  background-image: url("../../assets/little_icons/ms_office.png");
}
.python_logo {
  background-image: url("../../assets/little_icons/python.png");
}
.matlab_logo {
  background-image: url("../../assets/little_icons/matlab.png");
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
.tidyverse_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/tidyverse.png");
}
.ggplot_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/ggplot2.png");
}
.dplyr_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/dplyr.png");
}
.tidyr_logo {
  background-position: 0 -1px;

  background-image: url("../../assets/little_icons/tidyr.png");
}
.purrr_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/purrr.jpg");
}
.tensorflow_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/tens.png");
}
.tidymodels_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/tidymodels.png");
}
.sparklyr_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/sparklyr.png");
}
.stringr_logo {
  background-position: 0 -1px;
  background-image: url("../../assets/little_icons/stringr.png");
}
@media screen and (max-width: 1100px) {
  .skills {
    display: block;
    width: 50%;
    margin: 0 auto;
  }
  .skills:nth-of-type(2) {
    margin-top: 0px;
  }
  .skills > div {
    width: 100%;
    margin-top: 20px;
  }
}
@media screen and (max-width: 800px) {
  .skills {
    width: 90%;
  }
}
@media screen and (max-width: 460px) {
  .skills {
    width: 100%;
  }
  .coding_skills_container {
    width: 90%;
  }
  .python_card > h4,
  .matlab_card > h4,
  .r_card > h4,
  .latex_card > h4,
  .other_card h4 {
    padding-left: 5%;
  }
}
</style>