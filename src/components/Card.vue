<template>
  <div class="card">
    <figure class="card__img-wrapper">
      <img :src="src" :alt="alt" class="card__img">
    </figure><!-- /.card__img-wrapper -->
    <div class="card__body">
      <p class="card__text">{{ text }}</p><!-- /.card__text -->
    </div><!-- /.card__body -->
  </div><!-- /.card -->
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
      src: require(`../assets/${this.fileName}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .card {
    background-color: #fff;
    box-shadow: 0 0 6px #000;
    width: 320px;
  }

  .card__img-wrapper {
    position: relative;
    padding-top: 59.880%;
    overflow: hidden;
  }

  .card__img {
    position: absolute;
    top: 50%;
    left: 0;
    width: 100%;
    transform: translateY(-50%);
  }

  .card__body {
    padding: 25px 20px;
  }

  .card__text {
    color: #141414;
    text-align: left;
  }

  @media screen and (max-width: 1080px) {

    .card {
      max-width: 100%;
    }

  }
  
</style>
