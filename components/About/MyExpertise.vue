<template>
  <div>
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">My</span> Expertise
    </div>
    <div class="table-design vertical-border">
      <div
        v-for="(expertise, index) in my_expertise"
        :key="index"
        class="
          box-style
          flex-class flex-column
          horizontal-border
          position-relative
        "
      >
        <div class="icon flex-class"><i :class="iconClass(expertise)"></i></div>
        <div class="color-main expertise-heading">
          {{ expertise.expertise_heading }}
        </div>
        <div class="desc">
          <p>
            {{ expertise.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import myExpertise from "../../data/myExpertise.json";
export default {
  components: {},
  data() {
    return {
      my_expertise: myExpertise.myExpertise,
    };
  },
  methods: {
    iconClass(expertise) {
      return `fa fa-solid fa-${expertise.icon}`;
    },
  },
};
</script>

<style>
.icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #78cc6d;
  justify-content: center;
}
.flex-class {
  display: flex;
  align-items: center;
}
.flex-column {
  flex-direction: column;
}
.flex-row {
  flex-direction: row;
}
.icon .fa {
  font-size: 28px;
  color: #fff;
}
.expertise-heading {
  font-size: 18px;
  font-weight: 500;
  margin: 10px 0 5px 0;
  letter-spacing: 1px;
  width: auto;
  text-align: center;
}
.desc p {
  text-align: center;
}
.horizontal-border::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 1px;
  bottom: 0;
  left: 0;
  background: radial-gradient(
    ellipse at center,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 80%
  );
}
</style>