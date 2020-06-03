<template>
  <div class="container">
    <Navbar />
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
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  width: 100vw;
  position: relative;
  /* display: flex; */
  justify-content: center;
  /* align-items: center; */
  /* text-align: center; */
}



.links {
  padding-top: 15px;
}
</style>
