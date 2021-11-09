<template>
  <section class="concept" id="concept">
    <div class="concept__inner">
      <h2 class="concept__title">CONCEPT</h2><!-- /.concept__title -->
      <h3 class="concept__sub-title">
        “働きたくなる空間”をデザインすることで <br>
        人々を幸せにする。
      </h3><!-- /.concept__sub-title -->
      <div class="concept__container">
        <p class="concept__text">
          私たちは、オフィスに特化した空間デザイン専門としております。その理由は、「働きたくなる空間で仕事ができれば多くの人を幸せにできるのではないか」と考えるためです。そんな想いの株式会社Cresta Designだからこそできる空間デザインを提供させていただきます。  
        </p><!-- /.concept__text -->
        <img src="../assets/concept-image@2x.jpg" alt="" class="concept__img">
      </div><!-- /.concept__content -->
      <div class="concept__background-text">Our Concept</div><!-- /.concept__background-text -->
    </div><!-- /.concept__inner -->
  </section><!-- /.concept -->
</template>

<script>
export default {
  name: 'Concept'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .concept {

  }

  .concept__inner {
    padding: 100px 120px 70px 220px;
  }

  .concept__title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    text-align: left;
    margin-bottom: 70px;
    line-height: 0.8;
    letter-spacing: 0.05em;
  }

  .concept__title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #282F35;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }

  .concept__sub-title {
    font-size: 1.875rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 60px;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }

  .concept__container {
    display: flex;
    align-items: center;
    gap: 12%;
    margin-bottom: 70px;
    padding-right: 100px;
  }

  .concept__text {
    font-weight: bold;
    text-align: left;
    width: 44%;
    line-height: 1.875;
    letter-spacing: 0.05em;
  }

  .concept__img {
    width: 44%;
  }

  .concept__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(23,23,23,.05);
    text-align: right;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }

  @media screen and (max-width: 1080px) {

    .concept__inner {
    padding: 100px 120px 70px;
    }

    .concept__container {
      flex-direction: column;
      padding-right: 0;
    }
    
    .concept__text {
      width: 100%;
      margin-bottom: 30px;
    }

    .concept__img {
      width: 100%;
    }

  }

  @media screen and (max-width: 414px) {

    .concept__inner {
      padding: 100px 15px 40px;
    }

    .concept__title {
      font-size: 1.875rem;
    }

    .concept__title::after {
      width: 90px;
    }

    .concept__sub-title {
      font-size: 1.25rem;
    }

    .concept__background-text {
      font-size: 2.5rem;
    }

  }
  
</style>
