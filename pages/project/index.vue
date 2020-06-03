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
import Footer from "~/components/Footer.vue";
export default {
  components: {
    Navbar,
    Gallery,
    Footer
  }
}
</script>

<style>




.links {
  padding-top: 15px;
}
</style>
