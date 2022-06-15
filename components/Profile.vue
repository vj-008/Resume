<template>
  <div class="container border">
    <div class="border photo_align">Photo</div>
    <div class="border profile_description">
      <div class="name_font-size color-main">Varnika Jain</div>
      <!-- <div class="designation">Developer</div> -->
      <div class="container-type">
        <div class="typed-out">Web Developer</div>
      </div>
      <div class="social">
        <a href="https://github.com/vj-008" target="blank" class="social_icon">
          <i class="fa fa-github color-link"></i
        ></a>
        <a href="" target="blank" class="social_icon">
          <i class="fa fa-linkedin color-link"></i
        ></a>
        <a href="" target="blank" class="social_icon">
          <i class="fa fa-facebook color-link"></i
        ></a>
        <a href="" target="blank" class="social_icon">
          <i class="fa fa-instagram color-link"></i
        ></a>
      </div>
      <div class="contactme_profile">
        <nuxt-link
          :to="{
            path: 'contact',
          }"
          class="link_decoration color-link"
          >CONTACT ME</nuxt-link
        >
      </div>
    </div>
  </div>
</template>



<style>
/* .outer-background {
  background-color: bisque;
} */
.card-direction {
  display: flex;
  width: 85%;
  margin: auto;
  background-color: #fff;
  position: relative;
  top: 30px;
  align-items: center;
}
.container {
  width: 40%;
  height: 700px;
}
.border {
  border: 1px solid black;
}
.photo_align {
  height: 55%;
}
.profile_description {
  display: flex;
  align-items: center;
  flex-direction: column;
  height: 45%;
  position: relative;
}
.designation {
  margin-top: 10px;
}
.name_font-size {
  font-size: 2rem;
  margin-top: 1.3rem;
}
.social {
  padding: 15px;
  margin-top: 1.3rem;
}

.social_icon {
  margin: 0px 8px;
  font-size: 1.2rem;
}
.contactme_profile {
  border-top: 0.7px ridge rgb(137, 132, 132, 0.5);
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
  /* border-right: 0.15em solid orange; */
  white-space: nowrap;
  animation: typing 1s steps(20, end) forwards;
  font-size: 1.3rem;
  width: 0;
  color: #65c18c;
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