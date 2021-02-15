<template>
  <div class="contact" id="contact">
    <div class="content">
      <div class="mxw800p">
        <h3>{{ contactmodel.h3 }}</h3>
        <p>
          {{ contactmodel.p }}
        </p>
      </div>
      <div class="contactForm">
        <form>
          <div class="row">
            <div class="input50">
              <input type="text" placeholder="Full Name" required/>
            </div>
            <div class="input50">
              <input type="email" placeholder="Email Adress" required/>
            </div>
          </div>
          <div class="row">
            <div class="input100">
              <textarea placeholder="Message" required></textarea>
            </div>
          </div>
          <div class="row">
            <div class="input100">
              <input type="submit" value="Send" />
            </div>
          </div>
        </form>
      </div>
      <div class="social">
        <ul>
          <li>
            <a href="https://www.facebook.com/ls.gomes1994"><img src="@/assets/images/facebook.png" alt="" /></a>
          </li>
          <li>
            <a href="https://www.linkedin.com/in/lucas-dos-santos-gomes-a8a973194/"><img src="@/assets/images/linkedin.png" alt="" /></a>
          </li>
        </ul>
      </div>
       <div class="copyright">
        <p>Developed by <span>Lucas</span> | Credits for <a href="https://www.youtube.com/channel/UCbwXnUipZsLfUckBPsC7Jog">Online Tutorials</a></p>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    h3: String,
    contactmodel: Object,
  },
};
</script>

<style scoped>
.contact {
  background: #000;
  color: #fff;
  padding: 100px;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.contact .content {
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
  font-weight: lighter;
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
.contactForm {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
  display: flex;
}
.contactForm form {
  width: 100%;
}
.row {
  display: flex;
  width: 100%;
}
.input50{
    width: 50%;
    margin: 0 20px;
}
.input100{
    width: 100%;
    margin: 0 20px;
}
.input50 input,
.input100 input,
.input100 textarea{
    position: relative;
    border: none;
    border-bottom: 1px solid #fff;
    background: transparent;
    color: #fff;
    outline: none;
    width: 100%;
    padding: 10px;
    font-size: 18px;
    font-weight: 300;
    resize: none;
}
.input100 textarea{
    height: 100px;
}
.input50 input::placeholder,
.input100 input::placeholder,
.input100 textarea::placeholder{
    color: rgba(255, 255, 255, 0.5)
}
.input100 input[type="submit"]{
    background: #fff;
    color: #000;
    max-width: 100px;
    margin: none;
    text-transform: uppercase;
    letter-spacing: 2px;
    cursor: pointer;
    padding: 5px;
    margin-top: 20px;
}
.social{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 50px 0;
}
.social ul{
    display: flex;
}
.social ul li{
    list-style: none;
}
.social ul li a{
    text-decoration: none;
    display: inline-block;
    margin: 0 30px;
}
.social ul li a img{
    filter: invert(1);
    max-width: 40px;
}
.social ul li a:hover img{
    opacity: 0.5;
}
.copyright{
    color: #fff;
}
.copyright span{
    color: rgb(0, 119, 255);
    
}
.copyright a{
  text-decoration: none;  
  color: rgb(255, 0, 0);
}
@media (max-width: 960px) {
  .row{
    flex-direction: column;
    
  }
  .input50, .input100{
    width: 100%;
    margin: 20px 0;
  }
}
</style>