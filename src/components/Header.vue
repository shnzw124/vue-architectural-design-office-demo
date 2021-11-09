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
<style lang="scss" scoped>
  .Header {
    background-color: #282f35;
    font-style: italic;
    position: fixed;
    width: 100%;
    z-index: 10;
  }
  .Header_Inner {
    display: flex;
    justify-content: space-between;
    padding: 19px 120px;
  }
  .Header_Logo {
    font-size: 1.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.38462;
  }
  .Header_Nav {
    align-items: center;
    display: flex;
  }
  .Header_List {
    display: flex;
    list-style: none;
  }
  .Header_Item {
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.375;
    margin-right: 30px;
  }
  .Header_Item:last-child {
    margin-right: 0;
  }
  @media screen and (max-width: $sp) {
    .Header_Inner {
      padding: 19px 15px;
    }
    .Header_List {
      display: none;
    }
  }

</style>
