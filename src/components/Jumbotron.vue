<template>
  <figure class="jumbotron">
    <img :src="src" :alt="alt" class="jumbotron__img">
    <figcaption class="jumbotron__title">{{ text }}</figcaption><!-- /.jumbotron__title -->
  </figure><!-- /.jumbotron -->
</template>

<script>
export default {
  name: 'Jumbotron',
  props: {
    text: String,
    fileName: String,
    alt: String
  },
  data (){
    return {
      src: require(`../assets/${this.fileName}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .jumbotron {
    width: 33.33333%;
    height: auto;
    position: relative;
  }
  
  .jumbotron__img {
    position: absolute;
    top: 0;
    left: 0
  }

  .jumbotron__title {
    position: absolute;
    top: 50%;
    transform: translateY(-100%);
    left: 240px;
    transform: translateX(-50%);
    font-size: 40px;
    font-weight: bold;
    font-style: italic;
    color: #fff;
  }
  
</style>
