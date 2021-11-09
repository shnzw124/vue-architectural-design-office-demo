<template>
  <section class="Fv">
    <div class="Fv_Inner">
      <h1 class="Fv_Title">Design for Smile.</h1><!-- /.Fv_Title -->
      <p class="Fv_SubTitle">快適なオフィスを<br class="_sp-only">デザインする</p><!-- /.Fv_SubTitle -->
    </div><!-- /.Fv_Inner -->
    <swiper class="Fv_Background" :options="swiperOption">
      <swiper-slide class="Fv_BackgroundImg01"></swiper-slide>
      <swiper-slide class="Fv_BackgroundImg02"></swiper-slide>
      <swiper-slide class="Fv_BackgroundImg03"></swiper-slide>
    </swiper><!-- /.Fv_Background -->
  </section><!-- /.Fv -->  
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
<style lang="scss" scoped>
  .Fv {
    height: 752px;
    position: relative;
  }
  .Fv_Background {
    background-position: top center;
    background-size: cover;
    height: 752px;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
    z-index: -1;
  }
  .Fv_BackgroundImg01 {
    background-image: url("../assets/img/fv-bgi_01@2x.jpg");
  }
  .Fv_BackgroundImg02 {
    background-image: url("../assets/img/fv-bgi_02@2x.jpg");
  }
  .Fv_BackgroundImg03 {
    background-image: url("../assets/img/fv-bgi_03@2x.jpg");
  }
  .Fv_Inner {
    background: transparent;
    left: 120px;
    position: absolute;
    top: 409px;
  }
  .Fv_Title {
    color: #fff;
    font-size: 4.375rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: .71429;
    margin-bottom: 31px;
    text-align: center;
  }
  .Fv_SubTitle {
    color: #fff;
    font-size: 2.5rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.25;
    text-align: center;
  }
  ._sp-only {
    display: none;
  }
  @media screen and (max-width: $sp) {
    .Fv {
      height: 599px;
    }
    .Fv_Background {
      height: 599px;
    }
    .Fv_Inner {
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      width: 100%;
    }
    .Fv_Title {
      font-size: 2.3125rem;
      margin-bottom: 59px;
      text-align: center;
    }
    .Fv_SubTitle {
      font-size: 1.875rem;
      text-align: center;
    }
    ._sp-only {
      display: block;
    }
  }

</style>
