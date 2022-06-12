<template>
  <div>
    <div class="heading-style border color-main">
      <span class="color-primary">About</span> Me
    </div>
    <div class="table-design border">
      <div class="box-style">
        <p class="about-description">
          {{ about_me.description }}
        </p>
      </div>
      <ul class="box-style">
        <li
          class="box-element"
          v-for="list_item in about_me.list"
          :key="list_item"
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