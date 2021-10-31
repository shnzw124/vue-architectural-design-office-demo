<template>
  <section class="fv">
    <div class="fv__inner">
      <h1 class="fv__title">Design for Smile.</h1><!-- /.fv__title -->
      <p class="fv__sub-title">快適なオフィスを<br class="sp-only">デザインする</p><!-- /.fv__sub-title -->
    </div><!-- /.fv__inner -->
    <swiper class="fv__background" :options="swiperOption">
      <swiper-slide class="fv__background-img01"></swiper-slide>
      <swiper-slide class="fv__background-img02"></swiper-slide>
      <swiper-slide class="fv__background-img03"></swiper-slide>
    </swiper><!-- /.fv__background -->
  </section><!-- /.fv -->  
</template>

<script>
export default {
  name: 'FirstView',
  data() {
    return {
      swiperOption: {
        speed: 1000,//スライドの切り替わりスピード
        // spaceBetween: 30,//各スライドの余白
        centeredSlides: true,//スライダーを真ん中に
        loop: true, //無限ループ
        autoplay: { //スライドの自動切り替え
          delay: 5000,//スライドの自動切り替えの秒数
          disableOnInteraction: false//何らかのアクション後の自動切り替えを再開
        }
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .fv {
    position: relative;
    height: 752px;
  }
  
  .fv__background {
    position: absolute;
    /* top: 0; */
    /* left: 0; */
    background-size: cover;
    background-position: top center;
    height: 752px;
    width: 100%;
    z-index: -1;
  }

  .fv__background-img01 {
    background-image: url("../assets/fv-bgi_01@2x.jpg");
  }

  .fv__background-img02 {
    background-image: url("../assets/fv-bgi_02@2x.jpg");
  }

  .fv__background-img03 {
    background-image: url("../assets/fv-bgi_03@2x.jpg");
  }

  .fv__inner {
    position: absolute;
    /* top: 0; */
    /* left: 0; */
    background: transparent;
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
