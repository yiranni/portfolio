<template>
  <footer class="footer-container">
    <p id="footer">Copyright &copy; 2020 All Rights Reserved by Yiran Ni.</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
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
.footer-container {
  font-style: "Roboto", serif;
  position: absolute;
  bottom: 0;
  left: 0;
  height: 60px;
  width: 100%;
  background-color: white;
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 30px;
}
#footer {
    font-size: 12px;
    font-weight: 400;
}
</style>