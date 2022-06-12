<template>
  <div class="flex-class flex-column sidenav border">
    <div
      @click="setSelectedLink('about')"
      class="border sidenav-element flex-class flex-column"
    >
      <i class="fa fa-solid fa-user sidenav-icon"></i>
      ABOUT
    </div>
    <div
      @click="setSelectedLink('resume')"
      class="border sidenav-element flex-class flex-column"
    >
      <i class="fa fa-solid fa-file sidenav-icon"></i>
      RESUME
    </div>
    <div
      @click="setSelectedLink('contact')"
      class="border sidenav-element flex-class flex-column"
    >
      <i class="fa fa-solid fa-at sidenav-icon"></i>
      CONTACT
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    setSelectedLink(item) {
      this.$emit("selectedLink", item);
    },
  },
};
</script>
<style>
.sidenav {
  position: relative;
  top: -140px;
  margin-right: 15px;
}
.sidenav-icon {
  font-size: 18px;
  margin-bottom: 5px;
}

.sidenav-element {
  width: 100%;
  height: auto;
  padding: 16px 10px;
  cursor: pointer;
  font-size: 12px;
  color: #323232;
}
.sidenav-element:hover {
  color: #65c18c;
}
</style>