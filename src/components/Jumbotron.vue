<template>
  <div class="Jumbotron" :style="{ backgroundImage: 'url(' + imgPath + ')'}">
    <div class="Jumbotron_Inner">
      <p class="Jumbotron_Title">{{ text }}</p><!-- /.Jumbotron_Title -->
    </div><!-- /.Jumbotron_Inner -->
  </div><!-- /.Jumbotron -->
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
      imgPath: require(`../assets/img/${this.fileName}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Jumbotron {
    align-content: center;
    background-position: center center;
    background-size: cover;
    display: flex;
    flex-direction: column;
    height: 20vw;
    justify-content: center;
    max-height: 320px;
    width: 100%;
  }
  .Jumbotron_Title {
    color: #fff;
    font-size: 40px;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.25;
  }
  @media screen and (max-width: $tb) {
    .Jumbotron {
      height: 50vw;
      width: 100%;
    }
  }
  @media screen and (max-width: $sp) {
    .Jumbotron {
      height: 70vw;
      max-height: 250px;
      width: 100%;
    }
    .Jumbotron_Title {
      color: #fff;
      font-size: 1.25rem;
      font-style: italic;
      font-weight: bold;
    }
  }

</style>
