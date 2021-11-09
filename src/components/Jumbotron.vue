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
    line-height: 1.25;
    letter-spacing: 0.05em;
  }

  @media screen and (max-width: 1024px) {
    
    .jumbotron {
      width: 100%;
      height: 50vw;
    }

  }

  @media screen and (max-width: 414px) {
    
    .jumbotron {
      width: 100%;
      height: 70vw;
      max-height: 250px;
    }

    .jumbotron__title {
      font-size: 1.25rem;
      font-weight: bold;
      font-style: italic;
      color: #fff;
    }

  }
  
</style>
