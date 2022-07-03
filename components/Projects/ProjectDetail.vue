<template>
  <div>
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">P</span>rojects
    </div>
    <div
      class="pg-main position-relative horizontal-border"
      v-for="(project, index) in Projects"
      :key="index"
    >
      <div class="mb-1rem flex-class flex-row">
        <i :class="iconClass(project)"></i>
        <div class="ml-14 color-main">{{ project.title }}</div>
      </div>
      <div class="project-key-padding color-main project-key-font">
        Tools: <span class="project-value-font">{{ project.tools }}</span>
      </div>
      <div class="project-key-padding color-main project-key-font">
        Framework:
        <span class="project-value-font">{{ project.framework }}</span>
      </div>
      <div class="project-key-padding color-main project-key-font">
        Description:
        <span class="project-value-font">{{ project.description }}</span>
      </div>
    </div>
  </div>
</template>
<script>
import project from "../../data/project.json";
export default {
  name: "ProjectDetail",
  data() {
    return {
      Projects: project.projects,
    };
  },
  methods: {
    iconClass(project) {
      return `fa fa-solid ${project.icon} icon-font`;
    },
  },
};
</script>
<style>
.project-key-padding {
  padding: 6px 0px;
}
.project-key-font {
  font-size: 17px;
}
.project-value-font {
  font-size: 15px;
}
</style>
  
        
