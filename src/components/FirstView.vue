<template>
  <section class="fv">
    <div class="fv__inner">
      <h1 class="fv__title">Design for Smile.</h1><!-- /.fv__title -->
      <p class="fv__sub-title">快適なオフィスを<br class="sp-only">デザインする</p><!-- /.fv__sub-title -->
    </div><!-- /.fv__inner -->
  </section><!-- /.fv -->
</template>

<script>
export default {
  name: 'FirstView'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .fv {
    background-image: url("../assets/fv-bgi_01@2x.jpg");
    background-size: cover;
    background-position: top center;
    height: 752px;
  }

  .fv__inner {
    padding-top: 409px;
    padding-bottom: 177px;
    padding-left: 120px;
  }

  .fv__title {
    text-align: left;
    font-size: 4.375rem;
    font-weight: bold;
    color: #fff;
    margin-bottom: 31px;
  }

  .fv__sub-title {
    text-align: left;
    font-size: 2.5rem;
    font-weight: bold;
    font-style: italic;
    color: #fff;
  }

  .sp-only {
    display: none;
  }

  @media screen and (max-width: 414px) {

    .fv {
      height: 599px;
    }

    .fv__inner {
      padding-top: 202px;
      padding-bottom: 207px;
      padding-left: 15px;
    }

    .fv__title {
      text-align: center;
      font-size: 2.3125rem;
      margin-bottom: 59px;
    }

    .fv__sub-title {
      text-align: center;
      font-size: 1.875rem;
    }

    .sp-only {
      display: block;
    }

  }
  
</style>
