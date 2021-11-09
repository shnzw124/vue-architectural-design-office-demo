<template>
  <div class="Burger">
    <div class="Burger_Icon" v-on:click='active=!active'>
      <span class="Burger_Bar Burger_BarTop"    v-bind:class="{'_close': active}"></span>
      <span class="Burger_Bar Burger_BarMid"    v-bind:class="{'_close': active}"></span>
      <span class="Burger_Bar Burger_BarBottom" v-bind:class="{'_close': active}"></span>
    </div>
    <transition name="Burger_Menu">
      <div class="Burger_Wrapper" v-show="active">
        <nav class="Burger_Menu">
          <!-- TODO: v-forでレンダリング -->
          <ul class="Burger_List" @click="active=!active">
            <!-- TODO: urlとtextをpropsで渡す -->
            <li class="Burger_Item"><a href="#concept" class="Burger_Link">Concept</a></li>
            <li class="Burger_Item"><a href="#service" class="Burger_Link">Service</a></li>
            <li class="Burger_Item"><a href="#works"   class="Burger_Link">Works</a></li>
            <li class="Burger_Item"><a href="#contact" class="Burger_Link">Contact</a></li>
          </ul>
        </nav>
      </div>
    </transition>
  </div><!-- /.Burger -->
</template>

<script>
export default {
  name: 'Burger',
  props: {
    // text: String,
  },
  data() {
    return {
      active: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .Burger {
    display: none;
  }

  .Burger_Icon {
    border: none;
    display: block;
    height: 39px;
    position: relative;
    width: 39px;
    z-index: 3;
  }

  .Burger_Bar {
    background-color: #fff;
    display: block;
    height: 3px;
    left: 50%;
    position: absolute;
    transform: translateX(-50%);
    width: 20px;
  }

  .Burger_BarTop {
    top: 10px;
  }

  .Burger_BarMid {
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .Burger_BarBottom {
    bottom: 10px;
  }

  .Burger_Bar._close {
    background-color: #fff;
  }

  .Burger_BarTop._close {
    transform: translate(-50%, 10px) rotate(45deg);
    transition: transform .3s;
  }

  .Burger_BarMid._close {
    opacity: 0;
    transition: opacity .3s;
  }

  .Burger_BarBottom._close {
    transform: translate(-50%, -6px) rotate(-45deg);
    transition: transform .3s;
  }

  .Burger_Wrapper {
    height: 100vh;
    left: 0;
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 2;
  }

  .Burger_Menu {
    background-color: #282F35;
    height: 100%;
    width: 100%;
    z-index: 2;
  }

  .Burger_Menu .Burger_List {
    display: block;
    left: 50%;
    list-style: none;
    position: absolute;
    text-align: center;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .Burger_Menu .Burger_Item {
    margin-bottom: 40px;
    margin-right: 0;
  }

  .Burger_Item {
    font-style: italic;
    font-weight: bold;
    line-height: 1.375;
    letter-spacing: 0.05em;
  }

  .Burger_Link {
    color: #fff;
  }

  /* アニメーション */
  .Burger_Menu-enter-active, .Burger_Menu-leave-active {
    transition: opacity 0.4s;
  }
  
  .Burger_Menu-enter, .Burger_Menu-leave-to {
    opacity: 0;
  }
  
  .Burger_Menu-leave, .Burger_Menu-enter-to{
    opacity: 1;
  }

  @media screen and (max-width: 414px) {
    .Burger {
      display: block;
    }
  }
  
</style>
