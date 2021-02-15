<template>
    <div class="recentWorksCards">
        <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
         <div class="card">
            <a href="#"><h2>Work</h2></a>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.recentWorksCards{
  position: relative;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 20px;
  margin-top: 80px;
  max-width: 100%;
}
.card{
    position: relative;
    padding: 20px;
    width: 250px;
    min-height: 300px;
    margin: 0 auto;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
   
    
    box-shadow: 0 5px 30px rgba(0,0,0,0.5);
    border: transparent;
    background: rgb(0, 119, 255);
    color: #fff;
    transition: 0.5s;
}
.card:hover{
    background: #000;
    transition: 0.5s;
}
.card a{
    text-decoration: none;
    color: rgba(255, 255, 255, 0.4);
    text-transform: uppercase;
    font-size: 14px;
    letter-spacing: 1px;
}
.card a:hover{
    color: #fff;
}
@media (max-width: 960px) {
  
}

</style>