<template>
  <div class="container">
    <Navbar />
    <div id="start-wrapper">
      <p class="start">Design, Data, and Develop</p>
    </div>
    
    <Gallery />
    <Footer />
  </div>
</template>

<script>

import Navbar from "~/components/Navbar.vue"
import Gallery from "~/components/Gallery.vue"
import Footer from "~/components/Footer.vue"
export default {
  components: {
    Navbar,
    Gallery,
    Footer
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
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  width: 100vw;
  position: relative;
  justify-content: center;
}



.links {
  padding-top: 15px;
}

.start {
  font-family: 'Roboto', serif;
  margin-top: 60px;
  color: gray;
  font-weight: 500;
  font-size: 24px;
}

#start-wrapper {
  text-align: center;

}
</style>
