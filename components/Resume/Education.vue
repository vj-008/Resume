<template>
  <div>
    <div class="heading-style border color-main position-sticky">
      <span class="color-primary">R</span>esume
    </div>
    <div class="display-flex flex-row">
      <div class="width-50 border pg-main">
        <div class="mb-1rem flex-class flex-row border">
          <i class="fa fa-solid fa-briefcase icon-font"></i>
          <div class="ml-14 color-main">EXPERIENCE</div>
        </div>
        <div
          v-for="(experience, index) in resume.experience"
          :key="index"
          class="ptb-2rem"
        >
          <div class="years" :style="activeYear(experience)">
            {{ experience.year }}
          </div>
          <div class="color-main designation">
            {{ experience.designation }}
          </div>
          <div class="mb-14">{{ experience.company }}</div>
          <div>
            {{ experience.description }}
          </div>
        </div>
      </div>
      <div class="width-50 border pg-main">
        <div class="mb-1rem flex-class flex-row border">
          <i class="fa fa-solid fa-book icon-font"></i>
          <div class="ml-14 color-main">EDUCATION</div>
        </div>
        <div
          v-for="(education, index) in resume.education"
          :key="index"
          class="ptb-2rem"
        >
          <div class="years">{{ education.year }}</div>
          <div class="color-main designation">
            {{ education.designation }}
          </div>
          <div class="mb-14">{{ education.company }}</div>
          <div>
            {{ education.description }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import resume from "../../data/education.json";
export default {
  data() {
    return {
      resume: resume,
    };
  },
  methods: {
    activeYear(experience) {
      return {
        color: experience.color ? experience.color : "#646464",
        border: `1px solid ${experience.color}`,
        opacity: experience.opacity,
      };
    },
  },
};
</script>
<style>
.years {
  border: 0.5px solid #646464;
  width: fit-content;
  border-radius: 3px;
  font-size: 13px;
  padding: 0.5px 4px;
  margin-bottom: 1rem;
  letter-spacing: 0.5px;
  opacity: 0.5;
}
.ptb-2rem {
  padding: 2rem 0px;
}
.mb-1rem {
  margin-bottom: 1rem;
}
.designation {
  font-size: 16px;
  font-weight: 500;
}
.position-sticky {
  position: fixed;
  top: 0px;
  background: #fff;
  z-index: 2;
}
.mb-14 {
  margin-bottom: 14px;
}
.width-50 {
  width: 50%;
}
.ml-14 {
  font-weight: 500;
  margin-left: 14px;
}
.display-flex {
  display: flex;
}
</style>