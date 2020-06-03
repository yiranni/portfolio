<template>
  <div class="menu-wrapper">
    <div class="menu">
      <h4>Code</h4>
      <a href="https://github.com/yiranni" target="_blank">GitHub</a>
    </div>

    <div class="menu">
      <h4>Work</h4>
      <a href="https://www.linkedin.com/in/yiran-ni/" target="_blank">LinkedIn</a>
    </div>

    <div class="menu">
      <h4>Contact</h4>
      <a href="niy045@newschool.edu" target="_blank">niy045@newschool.edu</a>
    </div>
  </div>
</template>

<script>
export default {
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
.menu-wrapper {
  max-width: 300px;
  width: 100%;
  height: -webkit-fill-available;
  background-color: #242424;
  position: fixed;
  top: 0;
  right: 0;
  z-index: 50;
  font-family: "Roboto", serif;
  padding-top: 80px;
  padding-right: 30px;
  padding-left: 30px;
  transition: transform 0.3s ease;
  transform: translate(100%);
  overflow: hidden;
}
.menu-wrapper.active {
  transform: translate(0);
}
.menu-wrapper h4 {
  color: gray;
  font-size: 18px;
  padding-bottom: 8px;
}

.menu-wrapper a {
  color: white;
  text-decoration: underline;
}

.menu {
  margin-bottom: 30px;
}
</style>