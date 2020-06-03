<template>
  <div id="navbar">
    <ul id="pages">
      <li v-for="page in pages" :key="page.name">
        <nuxt-link :to="page.path">{{page.name}}</nuxt-link>
      </li>
    </ul>
    <button @click="toggleMenu()" :class="{'checked': checked}">{{menuText}}</button>
    <Menu :class="{'active': checked}"></Menu>
  </div>
</template>

<script>
import Menu from "~/components/Menu.vue";
export default {
  name: "Navbar",
  components: {
    Menu
  },
  data() {
    return {
      pages: [
        { name: "Overview", path: "/" },
        { name: "Projects", path: "/project" },
        { name: "About", path: "/about" }
      ],
      checked: false,
      menuText: "Menu"
    };
  },
  methods: {
    toggleMenu() {
      this.checked = !this.checked;
      this.menuText = this.checked ? "Close" : "Menu";
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
#navbar {
  width: 100%;
  top: 0;
  left: 0;
  background-color: white;
  display: flex;
  z-index: 100;
  font-family: "Roboto", serif;
  font-weight: 500;
  font-size: 16px;
}

#pages {
  list-style: none;
  padding-top: 20px;
  padding-bottom: 10px;
  padding-left: 0;
}

#pages li {
  display: inline;
  padding-left: 20px;
  padding-right: 10px;
}

a {
  text-decoration: none;
  color: black;
}

button {
  display: inline-block;
  border: none;
  background: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  font-family: "Roboto", serif;
  font-weight: 500;
  font-size: 16px;
  padding-top: 20px;
  padding-bottom: 10px;
  position: absolute;
  right: 20px;
  z-index: 100;
   top: 0;
  right: 20;
  
}

button:hover {
  cursor: pointer;
  color: gray;
}

button:focus {
  outline: 0;
}
.checked {
  color: gray;
}


</style>