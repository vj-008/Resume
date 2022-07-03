<template>
  <div class="right-card-container border">
    <project-detail></project-detail>
  </div>
</template>

<script>
import ProjectDetail from "./ProjectDetail.vue";
export default {
  components: { ProjectDetail },
  name: "Project",
};
</script>