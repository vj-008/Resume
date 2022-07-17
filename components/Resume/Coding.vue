<template>
  <div class="display-flex flex-row-direction vertical-border coding">
    <div class="width-50 pg-main">
      <div class="mb-1rem flex-class flex-row-direction">
        <i class="fa fa-solid fa-code icon-font"></i>
        <div class="ml-14 color-main">CODING</div>
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
</style>