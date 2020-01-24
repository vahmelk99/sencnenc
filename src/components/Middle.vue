<template>
  <div class="middle_all">
    <AboutSection :about="middle.about" />
    <Study :study="middle.study" />
    <Special :spec="middle.spec" />
    <CodingSkills />
    <Experience />
  </div>
</template>

<script>
import AboutSection from "./sections/AboutSection.vue";
import Study from "./sections/Study.vue";
import Experience from "./sections/Experience.vue";
import CodingSkills from "./sections/CodingSkills.vue";
import Special from "./sections/Special.vue";
export default {
  name: "Middle",
  data() {
    return {};
  },
  props: {
    middle: Object
  },
  components: {
    CodingSkills,
    Study,
    Experience,
    Special,
    AboutSection
  },
  created() {
    //request
  }
};
</script>