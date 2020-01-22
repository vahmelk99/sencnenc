<template>
  <div class="middle_all">
    <AboutSection />
    <Study />
    <Special />
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
  components: {
    CodingSkills,
    Study,
    Experience,
    Special,
    AboutSection
  }
};
</script>