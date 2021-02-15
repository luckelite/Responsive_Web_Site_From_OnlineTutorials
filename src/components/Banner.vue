<template>
  <section class="banner" id="home">
    <h2>We make<br /><span>brands</span> matter</h2>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.banner {
  position: relative;
  min-height: 100vh;
  background: url(bg.jpg);
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
}
.banner h2 {
  color: #fff;
  font-size: 90px;
  text-transform: uppercase;
  line-height: 1em;
  text-align: center;
}
.banner h2 span {
  color: rgb(0, 119, 255);
}
@media (max-width: 960px) {
  .banner {
    background-position: center;
  }
  .banner h2 {
    font-size: 60px;
    padding: 50px;
  }
}
</style>