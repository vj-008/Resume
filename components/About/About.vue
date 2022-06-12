<template>
  <div class="right-card-container border">
    <AboutMe></AboutMe>
    <MyExpertise></MyExpertise>
    <Interests></Interests>
    <Quote></Quote>
  </div>
</template>

<script>
import AboutMe from "../About/AboutMe.vue";
import MyExpertise from "~/components/About/MyExpertise.vue";
import Interests from "../About/Interests.vue";
import Quote from "../About/Quote.vue";
export default {
  components: {
    AboutMe,
    MyExpertise,
    Interests,
    Quote,
  },
};
</script>

<style>
.table-design {
  display: flex;
}
.box-style {
  padding: 2rem;
  width: 50%;
}
.about-description {
  line-height: 1.5;
}
.key-style {
  width: fit-content;
  padding: 2px 10px;
  background-color: #78cc6d;
  color: #fefefe;
  border-radius: 3px;
  letter-spacing: 2px;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
}

.box-element {
  margin-bottom: 20px;
}
.value-style {
  float: right;
  display: block;
  font-size: 17px;
  font-weight: 400;
}
ul {
  margin-bottom: 0px;
}
li {
  list-style: none;
}
/* .box-style li:before {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 1px;
  background: radial-gradient(
    ellipse at center,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 70%
  );
} */
</style>