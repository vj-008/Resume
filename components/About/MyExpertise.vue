<template>
  <div>
    <div class="heading-style border color-main">
      <span class="color-primary">My</span> Expertise
    </div>
    <div class="table-design border">
      <div
        v-for="expertise in my_expertise"
        :key="expertise"
        class="box-style border flex-class flex-column"
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
</style>