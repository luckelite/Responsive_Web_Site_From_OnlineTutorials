<template>
  <div class="cards">
    <div class="box">
      <div class="iconBox">
        <img :src="require('@/assets/images/' + cards.img )" alt="img" />
      </div>
      <div class="content">
        <h3>{{cards.h3}}</h3>
        <p>{{cards.p}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
        h3: String,
        p: String,
        img: String,
        cards: Object
    }
};
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.box{
    width: 300px;
    margin: 0 auto;
    background: #fff;
    padding: 20px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
}
.iconBox{
    margin-top: 25px;
    max-width: 70px;
    
}
.iconBox img{
    width: 100%;
    margin-bottom: 10px;
}
.content h3{
    margin-bottom: 15px;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 700;
}

</style>