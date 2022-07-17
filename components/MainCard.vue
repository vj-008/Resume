<template>
  <div class="outer-background">
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
import { doc } from "prettier";
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
</style>