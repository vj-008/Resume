<template>
  <div>
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">I</span>nterests
    </div>
    <div class="interest-table-design interest-container">
      <div
        v-for="(interest, index) in interest_values"
        :key="index"
        class="flex-class flex-column interest-element"
      >
        <div class="flex-class">
          <i :class="iconClass(interest)"></i>
        </div>
        <div class="interest-description">{{ interest.description }}</div>
      </div>
    </div>
  </div>
</template>
<script>
import interest from "../../data/interest.json";
export default {
  data() {
    return {
      interest_values: interest.interest,
    };
  },
  methods: {
    iconClass(interest) {
      return `fa fa-solid fa-${interest.icon_class} icon-font mb-15`;
    },
  },
};
</script>
<style>
.icon-font {
  font-size: 32px;
  color: #78cc6d;
}
.mb-15 {
  margin-bottom: 15px;
}
.interest-container {
  padding: 2rem 0px;
}
.interest-element {
  width: 25%;
  position: relative;
}
.interest-element:after {
  content: "";
  position: absolute;
  width: 1px;
  height: 150%;
  top: -2rem;
  left: 100%;
  background: radial-gradient(
    ellipse at top,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 70%
  );
}
.interest-description {
  font-size: 15px;
  font-weight: 500;
  letter-spacing: 1px;
}
.interest-table-design {
  display: flex;
}
</style>