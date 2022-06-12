<template>
  <div>
    <div class="heading-style border color-main">
      <span class="color-primary">I</span>nterests
    </div>
    <div class="border table-design interest-container">
      <div
        v-for="interest in interest_values"
        :key="interest"
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
  padding: 2rem;
}
.interest-element {
  padding: 2rem;
  width: 25%;
}
.interest-description {
  font-size: 15px;
  font-weight: 500;
  letter-spacing: 1px;
}
</style>