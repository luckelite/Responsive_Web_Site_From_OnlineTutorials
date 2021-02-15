<template>
  <div id="app">
    <Header />
    <Banner />
    <About :aboutmodel="about" :showbutton='true'/>
    <!--<About :aboutmodel="about2" :showbutton='false' :id="services"/>-->
    <Services :servicesmodel="services"/>
    <Achievements /> 
    <Portfolio :portfoliomodel="portfolio"/>
    <Contact :contactmodel="contact"/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Banner from "./components/Banner";
import About from "./components/About";
import Services from './components/Services';
import Achievements from './components/Achievements';
import Portfolio from './components/Portfolio';
import Contact from './components/Contact'

export default {
  name: "App",
  data() {
    return {
      about: {
        h3: "Who we Are",
        p:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
      },
      services: {
        h3: "What We Do",
        p:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      },
      portfolio: {
        h3: "Recent Works",
        p:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
      },
      contact: {
        h3: "Send Us a Message",
        p: "Lorem ipsum dolor sit amet"
      }
    };
  },
  components: {
    Header,
    Banner,
    About,
    Services,
    Achievements,
    Portfolio,
    Contact
  },
};
</script>

<style >
@import url("https://fonts.googleapis.com/css2?family=Prompt&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Prompt", sans-serif;
}
html {
  scroll-behavior: smooth;
}
body {
  min-height: 1000px;
  background: #000;
}

</style>
