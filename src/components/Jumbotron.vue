<template>
  <div class="jumbotron" :style="{ backgroundImage: 'url(' + imgPath + ')'}">
    <div class="jumbotron__inner">
      <p class="jumbotron__title">{{ text }}</p><!-- /.jumbotron__title -->
    </div><!-- /.jumbotron__inner -->
  </div><!-- /.jumbotron -->
</template>

<script>
export default {
  name: 'Jumbotron',
  props: {
    text: String,
    fileName: String,
  },
  data (){
    return {
      imgPath: require(`../assets/${this.fileName}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .jumbotron {
    width: 100%;
    height: 20vw;
    max-height: 320px;
    background-position: center center;
    background-size: cover;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
  }

  .jumbotron__title {
    font-size: 40px;
    font-weight: bold;
    font-style: italic;
    color: #fff;
  }
  
</style>
