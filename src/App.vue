<template>
  <div id="app">
    <Header/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue' 
export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
  #app {
    color: #282f35;
    font-family: "Noto Serif", "Noto Serif JP", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
  }
  a {
    color: #fff;
    text-decoration: none;
  }

</style>
