<template>
  <section class="sbfv">
    <div class="sbfv__inner">
      <h1 class="sbfv__title">{{ title }}</h1><!-- /.sbfv__title -->
      <div class="sbfv__background-text">{{ backgroundText }}</div><!-- /.sbfv__background-text -->
    </div><!-- /.sbfv__inner -->
  </section><!-- /.sbfv -->
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
  .sbfv {
    /* 背景画像もpropsで埋め込みたい */
    background-image: url("../assets/contact-page-bgi@2x.jpg");
    background-size: cover;
    background-position: top center;
    height: 453px;
  }

  .sbfv__inner {
    padding: 186px 48px 40px;
    position: relative;
  }

  .sbfv__title {
    text-align: center;
    font-size: 4.375rem;
    font-weight: bold;
    color: #fff;
    font-style: italic;
    line-height: 0.8;
    letter-spacing: 0.1em;
  }

  .sbfv__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }

  @media screen and (max-width: 414px) {

    .sbfv {
      height: 360px;
    }

    .sbfv__inner {
      padding-top: 175px;
      padding-bottom: 40px;
      padding-left: 15px;
    }

    .sbfv__title {
      text-align: center;
      font-size: 1.875rem;
      margin-bottom: 40px;
    }

    .sbfv__background-text {
      font-size: 2.5rem;
    }

  }
  
</style>
