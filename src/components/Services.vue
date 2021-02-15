<template>
  <section class="services" id="services">
    <div class="content">
      <div class="mxw800p">
        <h3>{{ servicesmodel.h3 }}</h3>
        <p>
          {{ servicesmodel.p }}
        </p>
      </div>
      <div class="cards">
        <CardServices :cards="card1" />
        <CardServices :cards="card2" />
        <CardServices :cards="card3" />
      </div>
    </div>
  </section>
</template>

<script>
import CardServices from "./CardServices";
export default {
  data() {
    return {
      card1: {
        h3: "Design",
        p: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
        img: "icon1.png"
      },
      card2: {
        h3: "Development",
        p: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
        img: "icon2.png"
      },
      card3: {
        h3: "Branding",
        p: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
        img: "icon3.png"
      },
    };
  },
  props: {
    h3: String,
    p: String,
    id: String,
    servicesmodel: Object,
  },
  components: {
    CardServices,
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.services {
  background: #fff;
  padding: 100px;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.services .content {
  position: relative;
  width: 100%;
  text-align: center;

}
.mxw800p {
  max-width: 800px;
  margin: 0 auto;
}
.mxw800p h3 {
  font-size: 2.4em;
  font-weight: 200;
  margin-bottom: 10px;
}
.mxw800p p {
  position: relative;
  font-size: 18px;
  font-weight: 200;
  margin-bottom: 20px;
  letter-spacing: 1px;
}
.mxw800p a {
  position: relative;
  display: inline-block;
  padding: 10px 30px;
  background: #000;
  color: #fff;
  text-decoration: none;
}
.cards{
    position: relative;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-gap: 20px;
    margin-top: 40px;
}
@media (max-width: 960px) {
  .services{
    padding: 100px 50px 50px 50px;
  }
  
}
</style>