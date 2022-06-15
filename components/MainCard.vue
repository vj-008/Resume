<template>
  <div class="outer-background">
    <div class="card-direction">
      <SideNav @selectedLink="setLink($event)"></SideNav>
      <Profile></Profile>
      <About v-if="selectedItem == 'about'"></About>
      <Resume v-if="selectedItem == 'resume'"></Resume>
      <Contact v-if="selectedItem == 'contact'"></Contact>
    </div>
  </div>
</template>
<script>
import about from "../components/About/About.vue";
export default {
  components: {
    about,
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