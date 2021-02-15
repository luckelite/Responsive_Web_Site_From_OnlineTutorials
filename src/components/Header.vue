<template>
  <header class="header">
    <a href="#home" class="logo">LOGO</a>
    <ul>
      <li><a href="#home" @click="toggle">Inicio</a></li>
      <li><a href="#about" @click="toggle">About</a></li>
      <li><a href="#services" @click="toggle">Services</a></li>
      <li><a href="#portfolio" @click="toggle">Portfolio</a></li>
      <li><a href="#contact" @click="toggle">Contact</a></li>
    </ul>
    <div class="toggle" @click="toggle"></div>
  </header>
</template>

<script>
window.addEventListener("scroll", () => {
  let header = document.querySelector("header");
  header.classList.toggle("sticky", window.scrollY > 0);
});

export default {
  methods: {
    toggle(){
      let header = document.querySelector("header");
      header.classList.toggle("active");
    }
  }
  
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 100px;
  z-index: 1000;
  transition: 0.5s;
}
header .logo {
  position: relative;
  font-weight: 700;
  letter-spacing: 2px;
  text-decoration: none;
  font-size: 2em;
  text-transform: uppercase;
  transition: 0.6s;
  color: #fff;
}
header  ul {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}
header ul li {
  position: relative;
  list-style: none;
}
header ul li a {
  position: relative;
  margin: 0 15px;
  color: #fff;
  font-weight: 300;
  letter-spacing: 2px;
  text-decoration: none;
  transition: 0.6s;
}
header ul li a:hover {
  color: rgb(0, 119, 255);
}
.sticky {
  padding: 5px 30px;
  background: #fff;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}
header.sticky .logo,
header.sticky ul li a {
  color: #000;
  font-weight: 700;
}
.toggle {
  display: none;
}
@media (max-width: 960px) {
  .toggle {
    display: block;
    position: relative;
    width: 30px;
    height: 30px;
    cursor: pointer;
  }
  .toggle:before {
    content: "";
    top: 4px;
    position: absolute;
    width: 100%;
    height: 3px;
    background: #000;
    z-index: 1;
    box-shadow: 0 10px 0 #000;
    transition: 0.5s;
  }
  .toggle:after {
    content: "";
    bottom: 3px;
    position: absolute;
    width: 100%;
    height: 3px;
    background: #000;
    z-index: 1;
    transition: 0.5s;
  }
  .header {
    padding: 5px 50px;
    background: #fff;
  }
  .header a{
    color: #000;
    font-weight: bold;
  }
  .header ul{
    position: absolute;
    top: 50px;
    left: 0;
    width: 100%;
    height: 100vh;
    text-align: center;
    display: block;
    overflow: auto;
    background: #fff;
    visibility: hidden;
    opacity: 0; 
  }
 .active ul {
    visibility: visible;
    opacity: 1;
    display: block;
    padding-top: 50px;
    transition: 0.5s;
  }
  .active ul li{
    padding: 10px;
    font-size: 1.5em;
  }
  
}
</style>