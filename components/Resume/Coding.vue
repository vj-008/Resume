<template>
  <div class="display-flex flex-row-direction vertical-border coding">
    <div class="width-50 pg-main">
      <div class="mb-1rem flex-class flex-row-direction">
        <i class="fa fa-solid fa-code icon-font"></i>
        <div class="ml-14 color-main">CODING</div>
      </div>
      <div class="display-flex circular-class">
        <div
          class="circular-progress"
          v-for="(framework, index) in coding"
          :key="index"
        >
          <v-progress-circular
            :value="framework.value"
            rotate="270"
            size="100"
            width="10"
            >{{ framework.value }}%</v-progress-circular
          >
          <div class="circular-text">{{ framework.text }}</div>
        </div>
      </div>
    </div>
    <div class="width-50 pg-main">
      <div class="mb-1rem flex-class flex-row-direction">
        <i class="fa fa-solid fa-list icon-font"></i>
        <div class="ml-14 color-main">KNOWLEDGE & SOFT SKILLS</div>
      </div>
      <ul class="list-padding">
        <li
          v-for="(list, index) in knowledge"
          :key="index"
          class="display-flex knowledge-alignment"
        >
          <div><i class="fa fa-solid fa-check list-icon"></i></div>
          <div class="list-margin">
            <p class="list-heading">{{ list.title }}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import coding from "../../data/coding.json";
export default {
  data() {
    return {
      knowledge: coding.knowledge,
      coding: coding.coding,
    };
  },
};
</script>
<style>
.list-padding {
  padding: 10px 0px;
}
.list-margin {
  margin-left: 1rem;
}
.list-heading {
  margin-bottom: 0.5rem;
}
.list-icon {
  color: #78cc6d;
  font-size: 22px;
}
.coding:after {
  display: block;
}
.v-progress-circular__underlay {
  stroke: #eeeeee;
}
.v-progress-circular__overlay {
  stroke: #78cc6d;
}
.circular-class {
  width: 100%;
  height: fit-content;
  flex-wrap: wrap;
}
.circular-progress {
  width: 50%;
  padding: 10px 20px 10px 0px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.circular-text {
  margin-top: 8px;
}
@media screen and (max-width:1100px) {
  .circular-class {
    flex-direction: column;
    align-items: center;
  }
}
</style>