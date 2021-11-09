<template>
  <section class="Sbfv">
    <div class="Sbfv_Inner">
      <h1 class="Sbfv_Title">{{ title }}</h1><!-- /.Sbfv_Title -->
      <div class="Sbfv_BackgroundText">{{ backgroundText }}</div><!-- /.Sbfv_BackgroundText -->
    </div><!-- /.Sbfv_Inner -->
  </section><!-- /.Sbfv -->
</template>

<script>
export default {
  name: 'SubFirstView',
  props: {
    title: String,
    backgroundText: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Sbfv {
    /* 背景画像もpropsで埋め込みたい */
    background-image: url("../assets/img/contact-page-bgi@2x.jpg");
    background-position: top center;
    background-size: cover;
    height: 453px;
  }
  .Sbfv_Inner {
    padding: 186px 48px 40px;
    position: relative;
  }
  .Sbfv_Title {
    color: #fff;
    font-size: 4.375rem;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .1em;
    line-height: .8;
    text-align: center;
  }
  .Sbfv_BackgroundText {
    color: rgba(255,255,255,.05);
    font-size: 5.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    text-align: left;
  }
  @media screen and (max-width: $sp) {
    .Sbfv {
      height: 360px;
    }
    .Sbfv_Inner {
      padding-bottom: 40px;
      padding-left: 15px;
      padding-top: 175px;
    }
    .Sbfv_Title {
      font-size: 1.875rem;
      margin-bottom: 40px;
      text-align: center;
    }
    .Sbfv_BackgroundText {
      font-size: 2.5rem;
    }
  }

</style>
