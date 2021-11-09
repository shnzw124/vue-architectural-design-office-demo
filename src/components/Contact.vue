<template>
  <section class="Contact" id="contact">
    <div class="Contact_Inner">
      <h2 class="Contact_Title">Contact</h2><!-- /.Contact_Title -->
      <p class="Contact_Text">お気軽にご相談ください。</p><!-- /.Contact_Text -->
      <div class="Contact_Btn">
        <Button text="Contact" url="./contact"></Button>
      </div><!-- /.Contact_Btn -->    
      <div class="Contact_BackgroundText">Contact us</div><!-- /.Contact_BackgroundText -->
    </div><!-- /.Contact_Inner -->
  </section><!-- /.Contact -->
</template>

<script>
import Button from './Button.vue' 

export default {
  name: 'Contact',
  components: {
    Button
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Contact {
    background-image: url("../assets/img/contact-bgi@2x.jpg");
    background-size: cover;
  }
  .Contact_Inner {
    padding: 104px 120px 70px;
  }
  .Contact_Title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    color: #fff;
    text-align: right;
    margin-bottom: 80px;
    transform: translateX(-230px);
    line-height: 0.8;
    letter-spacing: 0.1em;
  }
  .Contact_Title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #fff;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }
  .Contact_Text {
    font-size: 1.25rem;
    font-weight: bold;
    color: #fff;
    margin-bottom: 40px;
    line-height: 1.2;
    letter-spacing: 0.05em;
  }
  .Contact_Btn {
    margin-bottom: 70px;
  }
  .Contact_BackgroundText {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: $sp) {
    .Contact_Inner {
      padding: 100px 15px 40px;
    }
    .Contact_Title {
      font-size: 1.875rem;
      transform: translateX(-120px);
    }
    .Contact_Title::after {
      width: 90px;
    }
    .Contact_BackgroundText {
      font-size: 2.5rem;
    }
  }
</style>
