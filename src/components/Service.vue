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
    padding-top: 100px;
    padding-bottom: 80px;
  }

  .service__lower-inner {
    padding-top: 70px;
    padding-bottom: 70px;
  }

  .service__title {
    position: relative;
    font-size: 60px;
    font-weight: bold;
    font-style: italic;
    text-align: left;
    /* margin-bottom: 70px; */
    padding-left: 120px;
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
    /* margin-bottom: 70px; */
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  .service__jumbotron {
    width: 33.33333%;
  }

  .service__background-text {
    font-size: 90px;
    font-weight: bold;
    color: rgba(23,23,23,.05);
    text-align: right;
    padding-right: 120px;
  }
  
</style>
