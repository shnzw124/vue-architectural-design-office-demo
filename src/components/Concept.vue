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
        <img src="../assets/img/concept-image@2x.jpg" alt="" class="Concept_Img">
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
<style lang="scss" scoped>
  .Concept_Inner {
    padding: 100px 120px 70px 220px;
  }
  .Concept_Title {
    font-size: 3.75rem;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: .8;
    margin-bottom: 70px;
    position: relative;
    text-align: left;
  }
  .Concept_Title::after {
    border: 3px solid #282f35;
    content: "";
    display: inline-block;
    margin-left: 30px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 200px;
  }
  .Concept_SubTitle {
    font-size: 1.875rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    margin-bottom: 60px;
    text-align: center;
  }
  .Concept_Container {
    align-items: center;
    display: flex;
    gap: 12%;
    margin-bottom: 70px;
    padding-right: 100px;
  }
  .Concept_Text {
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.875;
    text-align: left;
    width: 44%;
  }
  .Concept_Img {
    width: 44%;
  }
  .Concept_BackgroundText {
    color: rgba(23,23,23,.05);
    font-size: 5.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    text-align: right;
  }
  @media screen and (max-width: $tb) {
    .Concept_Inner {
      padding: 100px 120px 70px;
    }
    .Concept_Container {
      flex-direction: column;
      padding-right: 0;
    }
    .Concept_Text {
      margin-bottom: 30px;
      width: 100%;
    }
    .Concept_Img {
      width: 100%;
    }
  }
  @media screen and (max-width: $sp) {
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
