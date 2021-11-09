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
<style lang="scss" scoped>
  .Service_UpperInner {
    padding: 100px 120px 0;
  }
  .Service_LowerInner {
    padding: 0 120px 70px;
  }
  .Service_Title {
    font-size: 3.75rem;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .1em;
    line-height: .8;
    margin-bottom: 70px;
    position: relative;
    text-align: left;
  }
  .Service_Title::after {
    border: 3px solid #282f35;
    content: "";
    display: inline-block;
    margin-left: 30px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 200px;
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
    color: rgba(23,23,23,.05);
    font-size: 5.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    text-align: right;
  }
  @media screen and (max-width: $tb) {
    .Service_Jumbotrons {
      flex-direction: column;
      margin-bottom: 40px;
    }
    .Service_Jumbotron {
      margin-bottom: 30px;
      margin-left: auto;
      margin-right: auto;
      width: 100%;
    }
    .Service_Jumbotron:last-child {
      margin-bottom: 0;
    }
  }
  @media screen and (max-width: $sp) {
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
