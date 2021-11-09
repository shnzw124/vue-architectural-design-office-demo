<template>
  <section class="Concept" id="concept">
    <div class="Concept_Inner">
      <h2 class="Concept_Title">CONCEPT</h2><!-- /.Concept_Title -->
      <h3 class="Concept_SubTitle">
        “働きたくなる空間”をデザインすることで <br>
        人々を幸せにする。
      </h3><!-- /.Concept_SubTitle -->
      <div class="Concept_Container">
        <p class="Concept_Text">
          私たちは、オフィスに特化した空間デザイン専門としております。その理由は、「働きたくなる空間で仕事ができれば多くの人を幸せにできるのではないか」と考えるためです。そんな想いの株式会社Cresta Designだからこそできる空間デザインを提供させていただきます。  
        </p><!-- /.Concept_Text -->
        <img src="../assets/concept-image@2x.jpg" alt="" class="Concept_Img">
      </div><!-- /.Concept_content -->
      <div class="Concept_BackgroundText">Our Concept</div><!-- /.Concept_BackgroundText -->
    </div><!-- /.Concept_Inner -->
  </section><!-- /.Concept -->
</template>

<script>
export default {
  name: 'Concept'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .Concept_Inner {
    padding: 100px 120px 70px 220px;
  }
  .Concept_Title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    text-align: left;
    margin-bottom: 70px;
    line-height: 0.8;
    letter-spacing: 0.05em;
  }
  .Concept_Title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #282F35;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }
  .Concept_SubTitle {
    font-size: 1.875rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 60px;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  .Concept_Container {
    display: flex;
    align-items: center;
    gap: 12%;
    margin-bottom: 70px;
    padding-right: 100px;
  }
  .Concept_Text {
    font-weight: bold;
    text-align: left;
    width: 44%;
    line-height: 1.875;
    letter-spacing: 0.05em;
  }
  .Concept_Img {
    width: 44%;
  }
  .Concept_BackgroundText {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(23,23,23,.05);
    text-align: right;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: 1080px) {
    .Concept_Inner {
      padding: 100px 120px 70px;
    }
    .Concept_Container {
      flex-direction: column;
      padding-right: 0;
    }
    .Concept_Text {
      width: 100%;
      margin-bottom: 30px;
    }
    .Concept_Img {
      width: 100%;
    }
  }
  @media screen and (max-width: 414px) {
    .Concept_Inner {
      padding: 100px 15px 40px;
    }
    .Concept_Title {
      font-size: 1.875rem;
    }
    .Concept_Title::after {
      width: 90px;
    }
    .Concept_SubTitle {
      font-size: 1.25rem;
    }
    .Concept_BackgroundText {
      font-size: 2.5rem;
    }
  }
</style>
