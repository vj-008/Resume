<template>
  <div class="right-card-container border">
    <div class="heading-style border color-main position-sticky">
      <span class="color-primary">Get </span>in Touch
    </div>
    <div>
      <ul class="contact-list">
        <li
          class="box-element"
          v-for="(list_item, index) in contact.list"
          :key="index"
        >
          <span class="key-style list-key-font">{{ list_item.key_item }}</span>
          <span class="value-style list-value-font">{{
            list_item.value_item
          }}</span>
        </li>
      </ul>
    </div>
    <!-- <div class="heading-style border color-main position-sticky">
      <span class="color-primary">S</span>ocial
    </div> -->
    <div class="social social-contact">
      <a href="https://github.com/vj-008" target="blank" class="social_icon">
        <i class="fa fa-github color-link icon-font-contact"></i
      ></a>
      <a href="" target="blank" class="social_icon">
        <i class="fa fa-linkedin color-link icon-font-contact"></i
      ></a>
      <a href="" target="blank" class="social_icon">
        <i class="fa fa-facebook color-link icon-font-contact"></i
      ></a>
      <a href="" target="blank" class="social_icon">
        <i class="fa fa-instagram color-link icon-font-contact"></i
      ></a>
    </div>
  </div>
</template>
<script>
import contact from "../../data/contact.json";
export default {
  data() {
    return {
      contact: contact.contact,
    };
  },
};
</script>
<style>
.contact-list {
  padding: 3rem 3rem 3rem 2rem;
}
.list-key-font {
  font-size: 16px;
}
.list-value-font {
  font-size: 19px;
}
.social-contact {
  width: fit-content;
  margin: auto;
}
.icon-font-contact {
  font-size: 1.5rem;
  margin-right: 20px;
}
</style>