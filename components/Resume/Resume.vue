<template>
  <div class="border right-card-container">
    <Education></Education>
    <MySkills></MySkills>
    <Coding></Coding>
  </div>
</template>
<script>
import Education from "~/components/Resume/Education.vue";
import MySkills from "~/components/Resume/MySkills.vue";
import Coding from "./Coding.vue";
export default {
  components: {
    Education,
    MySkills,
    Coding,
  },
};
</script>
<style>
</style>