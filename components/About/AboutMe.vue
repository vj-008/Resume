<template>
  <div>
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">About</span> Me
    </div>
    <div class="table-design vertical-border">
      <div class="box-style horizontal-border position-relative">
        <p class="about-description">
          {{ about_me.description }}
        </p>
      </div>
      <ul class="box-style horizontal-border position-relative">
        <li
          class="box-element position-relative"
          :class="[index == 3 ? '' : 'horizontal-border']"
          v-for="(list_item, index) in about_me.list"
          :key="index"
        >
          <span class="key-style">{{ list_item.key_item }}</span>
          <span class="value-style">{{ list_item.value_item }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import aboutMe from "../../data/aboutMe.json";
export default {
  data() {
    return {
      about_me: aboutMe.aboutMe,
    };
  },
};
</script>
<style >
.heading-style :after {
  content: "";
  position: absolute;
  display: block;
  width: 100%;
  height: 1px;
  left: -2rem;
  bottom: 0rem;
  background: radial-gradient(
    ellipse at left,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 80%
  );
}
.vertical-border {
  position: relative;
}
.vertical-border:after {
  content: "";
  position: absolute;
  width: 1px;
  height: 100%;
  left: 50%;
  background: radial-gradient(
    ellipse at top,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 90%
  );
}
</style>