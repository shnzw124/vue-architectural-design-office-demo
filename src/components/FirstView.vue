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
<style scoped>
  .Fv {
    position: relative;
    height: 752px;
  }
  .Fv_Background {
    position: absolute;
    top: 0;
    left: 0;
    background-size: cover;
    background-position: top center;
    height: 752px;
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
    position: absolute;
    top: 409px;
    left: 120px;
    background: transparent;
  }
  .Fv_Title {
    text-align: center;
    font-size: 4.375rem;
    font-weight: bold;
    color: #fff;
    margin-bottom: 31px;
    line-height: 0.71429;
    letter-spacing: 0.05em;
  }
  .Fv_SubTitle {
    text-align: center;
    font-size: 2.5rem;
    font-weight: bold;
    color: #fff;
    line-height: 1.25;
    letter-spacing: 0.05em;
  }
  ._sp-only {
    display: none;
  }
  @media screen and (max-width: 414px) {
    .Fv {
      height: 599px;
    }
    .Fv_Background {
      height: 599px;
    }
    .Fv_Inner {
      width: 100%;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
    .Fv_Title {
      text-align: center;
      font-size: 2.3125rem;
      margin-bottom: 59px;
    }
    .Fv_SubTitle {
      text-align: center;
      font-size: 1.875rem;
    }
    ._sp-only {
      display: block;
    }
  }
</style>
