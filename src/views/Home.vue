<template>
  <div class="Home">
    <FirstView/>
    <Concept/>
    <Works/>
    <Service/>
    <Contact/>
  </div>
</template>

<script>
import FirstView from '../components/FirstView.vue' 
import Concept from '../components/Concept.vue' 
import Works from '../components/Works.vue' 
import Service from '../components/Service.vue' 
import Contact from '../components/Contact.vue' 

export default {
  name: 'Home',
  components: {
    FirstView,
    Concept,
    Works,
    Service,
    Contact
  }
}
</script>
