<template>
  <section class="portfolio" id="portfolio">
    <div class="content">
      <div class="mxw800p">
        <h3>{{ portfoliomodel.h3 }}</h3>
        <p>
          {{ portfoliomodel.p }}
        </p>
      </div>
        <div class="recentWorks">
          <RecentWorksCards />
        </div>
    </div>
  </section>
</template>

<script>
import RecentWorksCards from "./RecentWorksCards";
export default {
  props: {
    h3: String,
    p: String,
    portfoliomodel: Object,
  },
  components: {
    RecentWorksCards,
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.portfolio {
  background: #fff;
  padding: 100px;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.portfolio .content {
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
@media (max-width: 960px) {
  .portfolio{
    padding: 100px 50px 50px 50px;
  }
}
</style>