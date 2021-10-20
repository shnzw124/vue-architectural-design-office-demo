<template>
  <section class="contact" id="contact">
    <div class="contact__inner">
      <h2 class="contact__title">Contact</h2><!-- /.contact__title -->
      <p class="contact__text">お気軽にご相談ください。</p><!-- /.contact__text -->
      <div class="contact__btn">
        <Button text="Contact" url=""></Button>
      </div><!-- /.contact__btn -->    
      <div class="contact__background-text">Contact us</div><!-- /.contact__background-text -->
    </div><!-- /.contact__inner -->
  </section><!-- /.contact -->
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
<style scoped>
  .contact {
    background-image: url("../assets/contact-bgi@2x.jpg");
    background-size: cover;
  }

  .contact__inner {
    padding: 104px 120px 70px;
  }

  .contact__title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    color: #fff;
    text-align: right;
    margin-bottom: 80px;
    transform: translateX(-230px);
  }

  .contact__title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #fff;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }

  .contact__text {
    font-size: 1.25rem;
    font-weight: bold;
    color: #fff;
    margin-bottom: 40px;
  }

  .contact__btn {
    margin-bottom: 70px;
  }

  .contact__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
  }

  @media screen and (max-width: 414px) {

    .contact__inner {
      padding: 100px 15px 40px;
    }

    .contact__title {
      font-size: 1.875rem;
      transform: translateX(-120px);
    }

    .contact__title::after {
      width: 90px;
    }

    .contact__sub-title {
      font-size: 1.25rem;
    }

    .contact__background-text {
      font-size: 2.5rem;
    }

  }

  
</style>
