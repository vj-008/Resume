<template>
  <div>
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">My</span> Skills
    </div>
    <div class="display-flex flex-row vertical-border">
      <div class="width-50 pg-main">
        <div class="mb-1rem flex-class flex-row">
          <i class="fa fa-solid fa-crop icon-font"></i>
          <div class="ml-14 color-main">TOOLS & SCM</div>
        </div>
        <div
          v-for="(framework, index) in skills.framework"
          :key="index"
          class="ptb-1rem"
        >
          <div class="title">{{ framework.title }}</div>
          <div class="background">
            <div
              class="block-progress"
              :style="{ width: framework.progress }"
            ></div>
          </div>
        </div>
      </div>
      <div class="width-50 pg-main">
        <div class="mb-1rem flex-class flex-row">
          <i class="fa fa-solid fa-flag icon-font"></i>
          <div class="ml-14 color-main">LANGUAGES</div>
        </div>
        <div
          v-for="(language, index) in skills.languages"
          :key="index"
          class="ptb-05rem"
        >
          <div class="title">{{ language.title }}</div>
          <div class="circle-background display-flex">
            <span
              v-for="circle in 10"
              :key="circle"
              class="circle-progress"
              :class="[circle < language.progress ? 'back-green' : 'back-grey']"
            ></span>
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
      skills: resume.skills,
    };
  },
};
</script>
<style>
.ptb-1rem {
  padding: 1rem 0px;
}
.ptb-05rem {
  padding: 0.8rem 0px;
}
.title {
  margin-bottom: 5px;
  font-size: 16px;
}
.background {
  width: 100%;
  height: 5px;
  background: #d8dbe2;
  position: relative;
  display: block;
}
.block-progress {
  position: absolute;
  left: 0;
  top: 0;
  background: #65c18c;
  height: 100%;
}
.circle-background {
  width: 100%;
  height: 14px;
  /* position: relative; */
}
.back-grey {
  background: #d8dbe2;
}
.back-green {
  background: #65c18c;
}
.circle-progress {
  top: 0;
  width: 14px;
  height: 14px;
  border-radius: 14px;
  margin-right: 4.5%;
}
</style>