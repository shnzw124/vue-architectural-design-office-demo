<template>
  <section class="service" id="service">
    <div class="service__upper-inner">
      <h2 class="service__title">Service</h2><!-- /.service__title -->
    </div><!-- /.service__upper-inner -->
    <div class="service__jumbotrons">
      <Jumbotron 
        class="service__jumbotron"
        text="Hearing"
        fileName="service-img01@2x.jpg">
      </Jumbotron>
      <Jumbotron
        class="service__jumbotron"
        text="Planning"
        fileName="service-img02@2x.jpg">
      </Jumbotron>
      <Jumbotron
        class="service__jumbotron"
        text="Direction"
        fileName="service-img03@2x.jpg">
      </Jumbotron>
    </div><!-- /.service__jumbotrons -->
    <div class="service__lower-inner">
      <div class="service__background-text">Our service</div><!-- /.service__background-text -->
    </div><!-- /.service__lower-inner -->
  </section><!-- /.service -->
</template>

<script>
import Jumbotron from './Jumbotron.vue'

export default {
  name: 'Service',
  components: {
    Jumbotron
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .service {

  }

  .service__upper-inner {
    padding: 100px 120px 0;
  }

  .service__lower-inner {
    padding: 0 120px 70px;
  }

  .service__title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    text-align: left;
    margin-bottom: 70px;
    line-height: 0.8;
    letter-spacing: 0.1em;
  }

  .service__title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #282F35;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }

  .service__jumbotrons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 70px;
  }

  .service__jumbotron {
    width: 33.33333%;
  }

  .service__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(23,23,23,.05);
    text-align: right;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }

  @media screen and (max-width: 1024px) {

    .service__jumbotrons {
      flex-direction: column;
      margin-bottom: 40px;
    }

    .service__jumbotron {
      width: 100%;
      margin-right: auto;
      margin-left: auto;
      margin-bottom: 30px;
    }

    .service__jumbotron:last-child {
      margin-bottom: 0;
    }
  }

  @media screen and (max-width: 414px) {

    .service__upper-inner {
      padding: 100px 15px 0;
    }

    .service__lower-inner {
      padding: 0 15px 64px;
    }

    .service__title {
      font-size: 1.875rem;
    }

    .service__title::after {
      width: 90px;
    }

    .service__sub-title {
      font-size: 1.25rem;
    }

    .service__background-text {
      font-size: 2.5rem;
    }

  }
  
</style>
