<template>
  <div class="container">
    <Navbar />
    <div class="about-wrapper">
      <div class="para">
        <div class="para-section">
          <h4>ABOUT ME</h4>
          <p>I’m Yiran Ni, a freelance data visualization designer and engineer. I create interactive visual forms to reveal, communicate, and tell stories about data. I enjoy helping people to literally see more about data, enabling exploration and greater understanding.</p>
        </div>
        <div class="para-section">
          <h4>EDUCATION</h4>
          <div class="edu-wrapper">
            <div class="year">
              <p>2019</p>
            </div>
            <div class="school">Parsons School of Design</div>
          </div>
          <div class="edu-wrapper">
            <div class="year">
              <p>2015</p>
            </div>
            <div class="school">University of Washington</div>
          </div>
        </div>
        <div class="para-section">
          <h4>SKILLS</h4>
          <div class="skill-wrapper">
            <div class="skill">
              <p class="skill-type">CODING</p>
              <p>Javascript</p>
              <p>D3.js</p>
              <p>P5.js</p>
              <p>three.js</p>
              <p>vue.js</p>
              <p>React.js</p>
              <p>jQuery</p>
              <p>Express.js</p>
              <p>AJAX</p>
              <p>Python</p>
              <p>R</p>
            </div>
            <div class="skill">
              <p class="skill-type">DESIGN</p>
              <p>Sketch</p>
              <p>Adobe InDesign</p>
              <p>Figma</p>
              <p>InVision</p>
              <p>Adobe Illustrator</p>
              <p>After Effects</p>
              <p>Photoshop</p>
            </div>
          </div>
        </div>
      </div>
      <div class="avatar">
        <img src="~/assets/img/yiran.png" />
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
export default {
  components: {
    Navbar,
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
};
</script>

<style>
.about-wrapper {
  padding: 2rem 1rem 1rem;
  max-width: 1000px;
  margin: 0px auto;
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  font-family: "Roboto", serif;
}

.avatar {
  width: 100%;
  /* display: block; */
  margin: 0 auto;
  padding-right: 3em;
  padding-left: 3em;
  justify-content: center;
  padding-top: 3em;
  align-items: center;
}

.avatar img {
  width: 100%;
}

.para {
  width: 100%;
  padding-top: 3em;
  padding-left: 3em;
  padding-right: 3em;
  padding-bottom: 10em;
}
.para-section {
  margin-bottom: 2em;
}

.para h4 {
  padding-bottom: 1em;
  font-size: 16px;
}

.para p {
  font-size: 14px;
  color: rgb(89, 89, 89);
  line-height: 20px;
}
.edu-wrapper {
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  font-size: 14px;
  color: rgb(89, 89, 89);
  height: 30px;
}

.year {
  width: 30%;
  font-weight: 500;
}

.school {
  width: 70%;
}

.skill-wrapper {
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  font-size: 14px;
  color: rgb(89, 89, 89);
  height: 30px;
}

.skill {
  width: 50%;
}

.skill-type {
    font-weight: 500;
    margin-bottom: 10px;
}
@media only screen and (min-width: 1024px) {
  .avatar {
    width: 50%;
    padding-top: 10em;
  }
  .para {
    width: 50%;
  }
}
</style>
