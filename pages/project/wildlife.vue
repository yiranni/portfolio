<template>
  <div class="container">
    <Navbar />

    <div class="project-wrapper">
      <h1 class="project-name">Global Journey of Zoonotic Diseases</h1>
      <div class="project-summary">
        <div class="project-info">
          <div class="info">
            <h4>TOOLS</h4>
            <p>vue.js</p>
            <p>d3.js</p>
          </div>

          <div class="info">
            <h4>CATEGORIES</h4>
            <p>Data Visualization</p>
            <p>Design</p>
            <p>Code</p>
            <p>Interation</p>
          </div>
          <div class="info">
            <h4>DATA VIZ</h4>
            <p>Choropleth Heatmap</p>
            <p>Pictorial Fraction Chart</p>
    <p>Donut Chart</p>
            <p>Dot Plot</p>
            <p>Lollipop Chart</p>
            <p>Pictorial Unit Chart</p>
            <p>Line Chart</p>
          </div>
          <div class="info">
            <h4>DATA</h4>
            <a
              href="https://trade.cites.org//"
              target="_blank"
            >CITES Trade Database</a>
          </div>
          <div class="info">
            <h4>LINK</h4>
            <a
              href="https://yiranni.github.io/master-thesis/#/"
              target="_blank"
            >Global Journey of Zoonotic Diseases</a>
          </div>
        </div>
        <div class="project-descr">
          <div class="descr">
           <p>COVID-19 has caused a worldwide pandemic in 2020. This pandemic brought the term “zoonotic diseases” to the public again. Zoonotic diseases are infectious diseases caused by germs that spread between animals and people with non-human animal origins, including SARS, Ebola, MERS, etc. </p>
            
            <p>Wildlife trading is one of the major transmission routes for zoonotic diseases. This data visualization analyzed <b>17 zoonotic diseases</b> and their <b>potential wildlife</b> reservoirs involved in trading in 2019. </p>
          <p style="font-size: 12px; color: gray">* The database only includes legal tradings reported to CITES by CITES member countries. </p>
          </div>
         
        </div>
      </div>
      <div class="project-demo"  >
        <img src="~/assets/img/demo/wildlife.png"/>
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
.project-wrapper {
  padding: 2rem 1rem 1rem;
  max-width: 1000px;
  margin: 0px auto;
  font-family: "Roboto", serif;
  margin-top: 2em;
}

.project-name {
  padding-bottom: 1em;
  font-size: 2.5em;
}
.project-demo {
  width: 100%;
  display: block;
  margin: 0 auto;
  padding-left: 10%;
  padding-right: 10%;
  margin-bottom: 4em;
}

.project-demo img {
  width: 100%;
}

.project-summary {
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
  padding-bottom: 2em;
}

.project-info {
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: row;
  flex-flow: wrap;
}

.info {
  width: 40%;
  min-height: 120px;
  margin-right: 10%;
}
.info h4 {
  padding-bottom: 1em;
}
.info p {
  color: gray;
  font-size: 14px;
}
.info a {
  font-size: 14px;
  color: gray;
}
.project-descr {
  width: 100%;
  position: relative;
}

.descr {
  min-height: 240px;
  width: 100%;
}

.descr a{
  color: black;
}

.descr p {
  margin-bottom: 16px;
}
@media only screen and (min-width: 1024px) {
  .project-info {
    width: 40%;
  }
  .project-descr {
    width: 60%;
  }
}
</style>
