<template>
  <div class="profile-container">
    <div class="photo_align">
      <img
        class="profile-image"
        src="@/assets/img/IMG_20210709_114540_006.jpeg"
        alt=""
      />
    </div>
    <div class="profile_description">
      <div class="name_font-size color-main">Varnika Jain</div>
      <!-- <div class="designation">Developer</div> -->
      <div class="container-type">
        <div class="typed-out">Web Developer</div>
      </div>
      <div class="social profile-border">
        <a href="https://github.com/vj-008" target="blank" class="social_icon">
          <i class="fa fa-github color-link"></i
        ></a>
        <a href="https://www.linkedin.com/in/varnika-jain-01547816b" target="blank" class="social_icon">
          <i class="fa fa-linkedin color-link"></i
        ></a>
        <a href="https://www.facebook.com/varnika.jain.507679" target="blank" class="social_icon">
          <i class="fa fa-facebook color-link"></i
        ></a>
        <a href="" target="blank" class="social_icon">
          <i class="fa fa-instagram color-link"></i
        ></a>
      </div>
      <div class="contactme_profile">
        <div
          class="link_decoration color-link"
          @click="setSelectedLink('contact')"
        >
          CONTACT ME
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    setSelectedLink(item) {
      this.$emit("selectedLink", { card: item, is_link: true });
    },
  },
};
</script>



<style>
.outer-background {
  background: linear-gradient(to bottom right, #50a3a2 0%, #78cc6d 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow-y: scroll;
  padding: 40px;
  width: 100%;
  position: relative;
}

.profile-container {
  width: 100%;
  height: 640px;
  border-radius: 5px;
  background-color: #fff;
  z-index: 10;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px,
    rgba(0, 0, 0, 0.04) 0px 10px 10px -5px, -10px -10px 0px 10px rgb(0 0 0 / 5%);
}
.border {
  border: 1px solid black;
}
.photo_align {
  height: 62%;
}
.profile_description {
  display: flex;
  align-items: center;
  flex-direction: column;
  height: 38%;
  position: relative;
}
.designation {
  margin-top: 10px;
}
.name_font-size {
  font-size: 2rem;
  margin-top: 1rem;
}
.social {
  padding: 15px;
  margin-top: 1rem;
}

.social_icon {
  margin: 0px 8px;
  font-size: 1.2rem;
}
.contactme_profile {
  width: 80%;
  padding: 15px;
  text-align: center;
  position: absolute;
  bottom: 10px;
}
.container-type {
  display: inline-block;
  margin-top: 10px;
}
.typed-out {
  overflow: hidden;
  white-space: nowrap;
  animation: typing 1s steps(20, end) forwards;
  font-size: 1.3rem;
  margin-left: 20px;
  width: 0;
  color: #65c18c;
}
.profile-image {
  width: 100%;
  height: 100%;
  border-radius: 5px;
  clip-path: polygon(0% 0%, 100% 0, 100% 80%, 50% 100%, 0 80%);
}
.profile-border::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 1px;
  left: 0;
  bottom: 70px;
  background: radial-gradient(
    ellipse at center,
    #dddddd 0%,
    rgba(255, 255, 255, 0) 80%
  );
}
@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}
</style>