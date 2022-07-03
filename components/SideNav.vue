<template>
  <div class="flex-class flex-column sidenav border">
    <button
      @click="setSelectedLink('about')"
      class="
        sidenav-element
        flex-class flex-column
        position-relative
        horizontal-border
      "
    >
      <i
        class="fa fa-solid fa-user sidenav-icon"
        :class="[active_button == 'about' ? 'active-link' : '']"
      ></i>
      <span
        class="text-icon"
        :class="[active_button == 'about' ? 'active-link' : '']"
        >ABOUT</span
      >
    </button>
    <button
      @click="setSelectedLink('resume')"
      class="
        sidenav-element
        flex-class flex-column
        position-relative
        horizontal-border
      "
    >
      <i
        class="fa fa-solid fa-file sidenav-icon"
        :class="[active_button == 'resume' ? 'active-link' : '']"
      ></i>
      <span
        class="text-icon"
        :class="[active_button == 'resume' ? 'active-link' : '']"
        >RESUME</span
      >
    </button>
    <button
      @click="setSelectedLink('project')"
      class="
        sidenav-element
        flex-class flex-column
        position-relative
        horizontal-border
      "
    >
      <i
        class="fa fa-solid fa-list sidenav-icon"
        :class="[active_button == 'project' ? 'active-link' : '']"
      ></i>
      <span
        class="text-icon"
        :class="[active_button == 'project' ? 'active-link' : '']"
        >PROJECTS</span
      >
    </button>
    <button
      @click="setSelectedLink('contact')"
      class="
        sidenav-element
        flex-class flex-column
        position-relative
        horizontal-border
      "
    >
      <i
        class="fa fa-solid fa-at sidenav-icon"
        :class="[active_button == 'contact' ? 'active-link' : '']"
      ></i>
      <span
        class="text-icon"
        :class="[active_button == 'contact' ? 'active-link' : '']"
        >CONTACT</span
      >
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active_button: "about",
    };
  },
  methods: {
    setSelectedLink(item) {
      this.active_button = item;
      this.$emit("selectedLink", item);
    },
  },
};
</script>
<style>
.sidenav {
  position: relative;
  top: -140px;
  margin-right: 10px;
  width: 67px;
  border-radius: 5px;
  background-color: #fff;
  z-index: 20;
}
.sidenav-icon {
  font-size: 15px;
  margin-bottom: 5px;
  font-weight: 600;
}
.active-link {
  color: #65c18c;
}
.sidenav-element {
  width: 100%;
  height: auto;
  padding: 13px 3px;
  cursor: pointer;
  font-size: 10px;
  color: #323232;
  font-weight: 600;
}
.sidenav-element:hover .sidenav-icon,
.sidenav-element:hover span {
  color: #65c18c;
}
</style>