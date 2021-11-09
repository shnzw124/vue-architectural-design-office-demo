<template>
  <div class="Card">
    <figure class="Card_ImgWrapper">
      <img :src="src" :alt="alt" class="Card_Img">
    </figure><!-- /.Card_ImgWrapper -->
    <div class="Card_Body">
      <p class="Card_Text">{{ text }}</p><!-- /.Card_Text -->
    </div><!-- /.Card_Body -->
  </div><!-- /.Card -->
</template>

<script>
export default {
  name: 'Card',
  props: {
    text: String,
    fileName: String,
    alt: String,
  },
  data (){
    return {
      // OK: src: require("../assets/card-img02@2x.jpg") 
      // NG: src: require(`${this.fileName}`) 
      // NG: src: require(this.fileName) 
      // NG: src: this.fileName 
      src: require(`../assets/img/${this.fileName}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Card {
    background-color: #fff;
    box-shadow: 0 0 6px #000;
    width: 320px;
  }
  .Card_ImgWrapper {
    overflow: hidden;
    padding-top: 59.880%;
    position: relative;
  }
  .Card_Img {
    left: 0;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
  }
  .Card_Body {
    padding: 25px 20px;
  }
  .Card_Text {
    color: #141414;
    letter-spacing: .05em;
    line-height: 1.875;
    text-align: left;
  }
  @media screen and (max-width: $tb) {
    .Card {
      max-width: 100%;
    }
  }

</style>
