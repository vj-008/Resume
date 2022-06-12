<template>
  <div>
    <div class="heading-style border color-main">
      <span class="color-primary">R</span>esume
    </div>
    <div class="display-flex flex-row">
      <div class="education-width border pg-main">
        <div class="flex-class flex-row">
          <i class="fa fa-solid fa-briefcase icon-font"></i>
          <div class="education-heading color-main">EXPERIENCE</div>
        </div>
        <div
          v-for="experience in resume.experience"
          :key="experience"
          class="education-element border"
        >
          <div class="years">{{ experience.year }}</div>
          <div class="color-main designation">
            {{ experience.designation }}
          </div>
          <div class="company">{{ experience.company }}</div>
          <div>
            {{ experience.description }}
          </div>
        </div>
      </div>
      <div class="education-width border pg-main">
        <div class="flex-class flex-row">
          <i class="fa fa-solid fa-book icon-font"></i>
          <div class="education-heading color-main">EDUCATION</div>
        </div>
        <div
          v-for="education in resume.education"
          :key="education"
          class="education-element border"
        >
          <div class="years">{{ education.year }}</div>
          <div class="color-main designation">
            {{ education.designation }}
          </div>
          <div class="company">{{ education.company }}</div>
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
};
</script>
<style>
.years {
  border: 1px solid #65c18c;
  width: fit-content;
  border-radius: 3px;
  font-size: 13px;
  color: #65c18c;
  padding: 0.5px 4px;
  margin-bottom: 1rem;
  letter-spacing: 0.5px;
}
.education-element {
  padding-top: 2rem;
}
.designation {
  font-size: 16px;
  font-weight: 500;
}
.company {
  margin-bottom: 14px;
}
.education-width {
  width: 50%;
}
.education-heading {
  margin-left: 14px;
}
.display-flex {
  display: flex;
}
</style>