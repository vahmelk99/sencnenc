<template>
  <div class="middle_all">
    <AboutSection :about="middle.about" />
    <Study :study="middle.study" />
    <Special :spec="middle.spec" />
    <CodingSkills :coding="middle.coding" />
    <Langs :langs="middle.langs" />
    <Experience :project="middle.project" />
    <Contact :contact="middle.contact" />
  </div>
</template>

<script>
import AboutSection from "./sections/AboutSection.vue";
import Study from "./sections/Study.vue";
import Experience from "./sections/Experience.vue";
import CodingSkills from "./sections/CodingSkills.vue";
import Special from "./sections/Special.vue";
import Langs from "./sections/Langs.vue";
import Contact from "./sections/Contact.vue";
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
    Contact,
    Experience,
    Special,
    AboutSection,
    Langs
  }
};
</script>