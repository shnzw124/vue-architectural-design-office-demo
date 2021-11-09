<template>
  <header class="Header">
    <div class="Header_Inner">
      <div class="Header_Logo"><a href="/" class="Header_Link">Cresta Design</a></div><!-- /.Header_Logo -->
      <nav class="Header_Nav">
        <ul class="Header_List">
          <li class="Header_Item">
            <a href="#concept" class="Header_Link">Concept</a><!-- /.Header_Link -->
          </li><!-- /.Header_Item -->
          <li class="Header_Item">
            <a href="#service" class="Header_Link">Service</a><!-- /.Header_Link -->
          </li><!-- /.Header_Item -->
          <li class="Header_Item">
            <a href="#works" class="Header_Link">Works</a><!-- /.Header_Link -->
          </li><!-- /.Header_Item -->
          <li class="Header_Item">
            <a href="#contact" class="Header_Link">Contact</a><!-- /.Header_Link -->
          </li><!-- /.Header_Item -->
        </ul><!-- /.Header_List -->
      </nav><!-- /.Header_Nav -->
      <Burger/>
    </div><!-- /.Header_Inner -->
  </header>
</template>

<script>
import Burger from './Burger.vue'
export default {
  components: { Burger },
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .Header {
    font-style: italic;
    position: fixed;
    width: 100%;
    background-color: #282F35;
    z-index: 10;
  }
  .Header_Inner {
    padding: 19px 120px;
    display: flex;
    justify-content: space-between;
  }
  .Header_Logo {
    font-size: 1.625rem;
    font-weight: bold;
    line-height: 1.38462;
    letter-spacing: 0.05em;
  }
  .Header_Nav {
    display: flex;
    align-items: center;
  }
  .Header_List {
    display: flex;
    list-style: none;
  }
  .Header_Item {
    margin-right: 30px;
    font-weight: bold;
    line-height: 1.375;
    letter-spacing: 0.05em;
  }
  .Header_Item:last-child {
    margin-right: 0;
  }
  @media screen and (max-width: 414px) {
    .Header_Inner {
      padding: 19px 15px;
    }
    .Header_List {
      display: none;
    }
  }
</style>
