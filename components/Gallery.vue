<template>
  <div>
    <div class="gallery-wrapper">
      <div v-for="project in projects" :key="project.name" class="project">
        <img :src="getImgUrl(project.img)" />
        <div class="project-name">{{project.name}}</div>
        <div class="project-year">{{project.year}}</div>
        <nuxt-link :to="project.path">
          <div class="hover-layer-top"></div>
          <div class="hover-layer-bottom"></div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import Projects from "~/assets/data/projects.json";
export default {
  name: "Gallery",
  data() {
    return {
      projects: Projects,
      project_hovered: false
    };
  },
  methods: {
    getImgUrl(end) {
      return require("../assets/img/" + end);
    }
  },
  head() {
    return {
      link: [
        {
          rel: "stylesheet",
          href:
            "https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&display=swap"
        },
        {
          rel: "stylesheet",
          href:
            "https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap"
        }
      ]
    };
  }
};
</script>

<style scoped>
.gallery-wrapper {
  display: flex;
  margin-top: 50px;
  flex-direction: row;
  flex-flow: wrap;
}
.project {
  width: 50vw;
  height: calc(50vw * 0.6);
  margin-bottom: 4px;
  font-family: "Roboto", serif;
  position: relative;
}

.project img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: grayscale(1) contrast(2) invert(1);
  opacity: 0.1;
}

.project:hover img {
  filter: none;
  opacity: 1;
}
.project-name {
  position: absolute;
  left: 20px;
  top: 40%;
  font-weight: 700;
  font-size: 28px;
  color: #242424;
}

.project:hover > .project-name,
.project:hover > .project-year {
  color: white;
}

.project-year {
  position: absolute;
  top: 10px;
  right: 20px;
  font-size: 14px;
  color: gray;
}

.project-name,
.project-year {
  z-index: 20;
}

.hover-layer-top {
  background-color: black;
  width: 100%;
  height: 0;
  position: absolute;
  top: 50%;
  left: 0;
  opacity: 0.8;
  transition: 0.3s ease;
}

.hover-layer-bottom {
  background-color: black;
  width: 100%;
  height: 0;
  position: absolute;
  bottom: 50%;
  left: 0;
  opacity: 0.8;
  transition: 0.3s ease;
  z-index: 10;
}

.project:hover .hover-layer-top {
  height: 50%;
}

.project:hover .hover-layer-bottom {
  height: 50%;
}

@media only screen and (min-width: 1200px) {
  .project {
    width: 25vw;
    height: 25vw;
  }
  .project-name {
    font-size: 24px;
  }
}
</style>