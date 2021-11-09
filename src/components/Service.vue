<template>
  <section class="Service" id="service">
    <div class="Service_UpperInner">
      <h2 class="Service_Title">Service</h2><!-- /.Service_Title -->
    </div><!-- /.Service_UpperInner -->
    <div class="Service_Jumbotrons">
      <Jumbotron 
        class="Service_Jumbotron"
        text="Hearing"
        fileName="service-img01@2x.jpg">
      </Jumbotron>
      <Jumbotron
        class="Service_Jumbotron"
        text="Planning"
        fileName="service-img02@2x.jpg">
      </Jumbotron>
      <Jumbotron
        class="Service_Jumbotron"
        text="Direction"
        fileName="service-img03@2x.jpg">
      </Jumbotron>
    </div><!-- /.Service_Jumbotrons -->
    <div class="Service_LowerInner">
      <div class="Service_BackgroundText">Our service</div><!-- /.Service_BackgroundText -->
    </div><!-- /.Service_LowerInner -->
  </section><!-- /.Service -->
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
  .Service_UpperInner {
    padding: 100px 120px 0;
  }
  .Service_LowerInner {
    padding: 0 120px 70px;
  }
  .Service_Title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    text-align: left;
    margin-bottom: 70px;
    line-height: 0.8;
    letter-spacing: 0.1em;
  }
  .Service_Title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #282F35;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }
  .Service_Jumbotrons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 70px;
  }
  .Service_Jumbotron {
    width: 33.33333%;
  }
  .Service_BackgroundText {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(23,23,23,.05);
    text-align: right;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: 1024px) {
    .Service_Jumbotrons {
      flex-direction: column;
      margin-bottom: 40px;
    }
    .Service_Jumbotron {
      width: 100%;
      margin-right: auto;
      margin-left: auto;
      margin-bottom: 30px;
    }
    .Service_Jumbotron:last-child {
      margin-bottom: 0;
    }
  }
  @media screen and (max-width: 414px) {
    .Service_UpperInner {
      padding: 100px 15px 0;
    }
    .Service_LowerInner {
      padding: 0 15px 64px;
    }
    .Service_Title {
      font-size: 1.875rem;
    }
    .Service_Title::after {
      width: 90px;
    }
    .Service_BackgroundText {
      font-size: 2.5rem;
    }
  }
</style>
