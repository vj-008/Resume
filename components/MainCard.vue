<template>
  <div class="outer-background">
      <ul class="bg-bubbles">
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
    <div class="top-name">Varnika Jain</div>
    <div class="flex-class left-width">
      <SideNav @selectedLink="setLink($event)" :contact="contact"></SideNav>
      <Profile
        class="position-relative"
        @selectedLink="setLink($event)"
      ></Profile>
    </div>
    <About
      v-if="selectedItem == 'about' || isSmall"
      class="slide"
      id="about"
    ></About>
    <Resume
      v-if="selectedItem == 'resume' || isSmall"
      class="slide"
      id="resume"
    ></Resume>
    <project
      v-if="selectedItem == 'project' || isSmall"
      class="slide"
      id="project"
    ></project>
    <Contact
      v-if="selectedItem == 'contact' || isSmall"
      class="slide"
      id="contact"
    ></Contact>
  </div>

</template>
<script>
import about from "../components/About/About.vue";
import project from "../components/Projects/Project.vue";
export default {
  components: {
    about,
    project,
  },
  data() {
    return {
      selectedItem: "about",
      is_small: false,
      contact: false,
    };
  },
  created() {
    window.addEventListener("resize", this.windowWidth);
  },
  mounted() {
    if (window.screen.width < 1435) {
      this.is_small = true;
    }
  },
  destroyed() {
    window.removeEventListener("resize", this.windowWidth);
  },
  computed: {
    isSmall() {
      return this.is_small;
    },
  },
  methods: {
    setLink(item) {
      let element = null;
      if (window.screen.width < 1435) {
        element = document.getElementById(`${item.card}`);
        element.scrollTop = element.scrollHeight;
        if (element) {
          element.scrollIntoView({
            behavior: "smooth",
          });
        }
      } else {
        this.contact = item.is_link;
        this.selectedItem = item.card;
      }
    },
    windowWidth() {
      if (window.screen.width < 1435) {
        this.is_small = true;
      } else {
        this.is_small = false;
      }
    },
  },
};
</script>
<style>
.slide {
  position: absolute;
  left: 0px;
  animation: mymove 1.5s ease;
  z-index: 0;
}
.left-width {
  width: 40%;
}
.top-name {
  display: none;
}
.bg-bubbles{
  /* position: absolute;
  bottom: -320px; */
    /* top: 0;
    left: 0; */
    /* width: 100%;
    height: 100%; */
}
.bg-bubbles li{
    position: absolute;
    list-style: none;
    display: block;
    width: 80px;
    height: 80px;
    background-color: rgba(255, 255, 255, 0.1);
    bottom: 0px;
    animation: square 50s infinite;
    
    transition-timing-function: linear;
}
li{
  margin-bottom: 0px;
}
.bg-bubbles li:nth-child(1) {
  left: 10%;
}
.bg-bubbles li:nth-child(2) {
  left: 20%;
  width: 160px;
  height: 160px;
  animation-delay: 2s;
  animation-duration: 34s;
}
.bg-bubbles li:nth-child(3) {
  left: 25%;
  animation-delay: 4s;
}
.bg-bubbles li:nth-child(4) {
  left: 40%;
  width: 120px;
  height: 120px;
  animation-delay: 44s;
}
.bg-bubbles li:nth-child(5) {
  left: 70%;
}
.bg-bubbles li:nth-child(6) {
  left: 80%;
  width: 240px;
  height: 240px;
  animation-delay: 3s;
}
.bg-bubbles li:nth-child(7) {
  left: 32%;
  width: 320px;
  height: 320px;
  animation-delay: 7s;
}
.bg-bubbles li:nth-child(8) {
  left: 55%;
  width: 40px;
  height: 40px;
  animation-delay: 15s;
  animation-duration: 80s;
}
.bg-bubbles li:nth-child(9) {
  left: 25%;
  width: 20px;
  height: 20px;
  animation-delay: 2s;
  animation-duration: 80s;
}
.bg-bubbles li:nth-child(10) {
  left: 90%;
  width: 320px;
  height: 320px;
  animation-delay: 22s;
}


@keyframes mymove {
  from {
    left: -30%;
    opacity: 0.1;
  }
  to {
    left: 0;
    opacity: 1;
  }
}

@keyframes square {
  0%{
    transform: translateY(0);
  }
  100%{
        transform: translateY(-1500px) rotate(600deg);
  }
}
</style>