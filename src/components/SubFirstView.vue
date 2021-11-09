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
<style scoped>
  .Sbfv {
    /* 背景画像もpropsで埋め込みたい */
    background-image: url("../assets/img/contact-page-bgi@2x.jpg");
    background-size: cover;
    background-position: top center;
    height: 453px;
  }
  .Sbfv_Inner {
    padding: 186px 48px 40px;
    position: relative;
  }
  .Sbfv_Title {
    text-align: center;
    font-size: 4.375rem;
    font-weight: bold;
    color: #fff;
    font-style: italic;
    line-height: 0.8;
    letter-spacing: 0.1em;
  }
  .Sbfv_BackgroundText {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: 414px) {
    .Sbfv {
      height: 360px;
    }
    .Sbfv_Inner {
      padding-top: 175px;
      padding-bottom: 40px;
      padding-left: 15px;
    }
    .Sbfv_Title {
      text-align: center;
      font-size: 1.875rem;
      margin-bottom: 40px;
    }
    .Sbfv_BackgroundText {
      font-size: 2.5rem;
    }
  }
</style>
