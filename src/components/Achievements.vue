<template>
  <div id="achievements">
    <div class="content">
      <div class="mxw800p">
        <h3>Our Achievements</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam.
        </p>
      </div>
      <div class="boxes">
          <div class="box">
              <h2>1200+</h2>
              <h4>Projects</h4>
          </div>
          <div class="box">
              <h2>150+</h2>
              <h4>Countries</h4>
          </div>
          <div class="box">
              <h2>800+</h2>
              <h4>Happy Clients</h4>
          </div>
          <div class="box">
              <h2>50+</h2>
              <h4>Awards</h4>
          </div>
      </div>
    </div>
  </div>
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
#achievements {
  min-height: 100vh;
  margin-top: -250px;
  padding-top: 250px;
  background: #000;
  color: #fff;

  display: flex;
  justify-content: center;
  align-items: center;
}
.content {
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
.boxes{
    position: relative;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 20px;
    max-width: 100%;
    margin-top: 40px;
}
.box h2{
    font-size: 25px;
    font-weight: bold;
    letter-spacing: 2px;
}
.box h4{
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 3px;
    text-transform: uppercase;
}
@media (max-width: 960px) {
  .achievements{ 
    padding: 100px 50px 50px 50px;
  }
}
</style>