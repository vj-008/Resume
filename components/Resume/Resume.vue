<template>
  <div class="border right-card-container">
    <Education></Education>
    <MySkills></MySkills>
  </div>
</template>
<script>
import Education from "~/components/Resume/Education.vue";
import MySkills from "~/components/Resume/MySkills.vue";
export default {
  components: {
    Education,
    MySkills,
  },
};
</script>
<style>
</style>