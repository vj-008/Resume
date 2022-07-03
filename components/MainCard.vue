<template>
  <div class="outer-background">
    <div class="card-direction">
      <SideNav @selectedLink="setLink($event)"></SideNav>
      <Profile class="position-relative"></Profile>
      <About v-if="selectedItem == 'about'" class="slide"></About>
      <Resume v-if="selectedItem == 'resume'" class="slide"></Resume>
      <project v-if="selectedItem == 'project'" class="slide"></project>
      <Contact v-if="selectedItem == 'contact'" class="slide"></Contact>
    </div>
  </div>
</template>
<script>
import about from "../components/About/About.vue";
import project from "../components/Projects/Project.vue";
export default {
  components: {
    about,
    project,
  },
  data() {
    return {
      selectedItem: "about",
    };
  },
  methods: {
    setLink(item) {
      this.selectedItem = item;
    },
  },
};
</script>
<style>
.slide {
  position: absolute;
  left: 0px;
  animation: mymove 1.5s ease;
  z-index: 0;
}
@keyframes mymove {
  from {
    left: -30%;
    opacity: 0.1;
  }
  to {
    left: 0;
    opacity: 1;
  }
}
</style>