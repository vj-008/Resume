<template>
  <div class="right-card-container border">
    <div class="heading-style color-main position-sticky">
      <span class="color-primary">Get </span>in Touch
    </div>
    <!-- <div class="map-align">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d27805.569844073154!2d77.17657538725936!3d29.408441191206496!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390dd32d31e7c90b%3A0xb701fcd1d770e6bd!2sKairanaa%20Rural%2C%20Uttar%20Pradesh%20247774!5e0!3m2!1sen!2sin!4v1656760119651!5m2!1sen!2sin"
        width="654"
        height="400"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </div> -->
    <div>
      <ul class="contact-list position-relative horizontal-border">
        <li
          class="box-element-contact position-relative horizontal-border"
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
  font-size: 16px;
}
.social-contact {
  width: fit-content;
  margin: auto;
}
.icon-font-contact {
  font-size: 1.5rem;
  margin-right: 20px;
}
.map-align {
  padding-top: 40px;
  align-items: center;
  justify-content: center;
  display: flex;
}
.box-element-contact {
  padding: 15px 0px;
}
</style>