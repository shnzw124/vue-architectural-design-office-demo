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
    color: #fff;
    font-size: 3.75rem;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .1em;
    line-height: .8;
    margin-bottom: 80px;
    position: relative;
    text-align: right;
    transform: translateX(-230px);
  }
  .Contact_Title::after {
    border: 3px solid #fff;
    content: "";
    display: inline-block;
    margin-left: 30px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 200px;
  }
  .Contact_Text {
    color: #fff;
    font-size: 1.25rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.2;
    margin-bottom: 40px;
  }
  .Contact_Btn {
    margin-bottom: 70px;
  }
  .Contact_BackgroundText {
    color: rgba(255,255,255,.05);
    font-size: 5.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    text-align: left;
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
