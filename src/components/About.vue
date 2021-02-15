<template>
  <section class="about" id="about">
    <div class="content">
      <div class="mxw800p">
        <h3>{{aboutmodel.h3}}</h3>
        <p>
          {{aboutmodel.p}}
        </p>
        <a href="#" v-if="showbutton === true">Read our history</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    props: {
        h3: String,
        p: String,
        showbutton: Boolean, 
        aboutmodel: Object
    }
};
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.about{
    background: #fff;
    padding: 100px;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.about .content{
    position: relative;
    width: 100%;
    text-align: center;
}
.mxw800p{
    max-width: 800px;
    margin: 0 auto;
}
.mxw800p h3{
    font-size: 2.4em;
    font-weight: 200;
    margin-bottom: 10px;
}
.mxw800p p{
    position: relative;
    font-size: 18px;
    font-weight: 200;
    margin-bottom: 20px;
    letter-spacing: 1px;
}
.mxw800p a{
    position: relative;
    display: inline-block;
    padding: 10px 30px;
    background: #000;
    color: #fff;
    text-decoration: none;
}
@media (max-width: 960px) {
  .about{
    padding: 100px 50px 50px 50px;
  }
}
</style>