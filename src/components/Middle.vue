<template>
  <div class="middle_all">
    <AboutSection />
    <Study />
    <Experience />
    <CodingSkills />
  </div>
</template>

<script>
import AboutSection from "./sections/AboutSection.vue";
import Study from "./sections/Study.vue";
import Experience from "./sections/Experience.vue";
import CodingSkills from "./sections/CodingSkills.vue";
export default {
  name: "Middle",
  components: {
    CodingSkills,
    Study,
    Experience,
    AboutSection
  }
};
</script>