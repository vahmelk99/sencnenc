<template>
  <div class="middle_all">
    <AboutSection />
    <Study />
    <Experience />
  </div>
</template>

<script>
import AboutSection from "./sections/AboutSection.vue";
import Study from "./sections/Study.vue";
import Experience from "./sections/Experience.vue";
export default {
  name: "Middle",
  components: {
    Study,
    Experience,
    AboutSection
  },
  data() {
    return {};
  }
};
</script>