<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header/>
    <FirstView/>
    <Concept/>
    <Works/>
    <!-- <Service/> -->
    <Contact/>
    <Footer/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import FirstView from './components/FirstView.vue' 
import Concept from './components/Concept.vue' 
import Works from './components/Works.vue' 
// import Service from './components/Service.vue' 
import Contact from './components/Contact.vue' 
import Footer from './components/Footer.vue' 

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Header,
    FirstView,
    Concept,
    Works,
    // Service,
    Contact,
    Footer
  }
}
</script>

<style>
#app {
  font-family: "Noto Serif", "Noto Serif JP", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #282F35;
}
</style>
