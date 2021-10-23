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
    padding-top: 186px;
    padding-bottom: 185px;
    position: relative;
  }

  .sbfv__title {
    text-align: center;
    font-size: 4.375rem;
    font-weight: bold;
    color: #fff;
    font-style: italic;
  }

  .sbfv__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
    position: absolute;
    top: 283px;
    left: 48px;
  }

  @media screen and (max-width: 414px) {

    .sbfv {
      height: 599px;
    }

    .sbfv__inner {
      padding-top: 202px;
      padding-bottom: 207px;
      padding-left: 15px;
    }

    .sbfv__title {
      text-align: center;
      font-size: 2.3125rem;
      margin-bottom: 59px;
    }

    .sbfv__background-text {

    }

  }
  
</style>
