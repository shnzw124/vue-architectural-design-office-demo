<template>
  <div class="burger">
    <div class="burger__icon" v-on:click='active=!active'>
      <span class="burger__bar burger__bar-top" v-bind:class="{'close': active}"></span>
      <span class="burger__bar burger__bar-mid" v-bind:class="{'close': active}"></span>
      <span class="burger__bar burger__bar-bottom" v-bind:class="{'close': active}"></span>
    </div>
    <transition name="burger__menu">
      <div class="burger__wrapper" v-show="active">
        <nav class="burger__menu">
          <!-- TODO: v-forでレンダリング -->
          <ul class="burger__list" @click="active=!active">
            <!-- TODO: urlとtextをpropsで渡す -->
            <li class="burger__item"><a href="#concept" class="burger__link">Concept</a></li>
            <li class="burger__item"><a href="#service" class="burger__link">Service</a></li>
            <li class="burger__item"><a href="#works" class="burger__link">Works</a></li>
            <li class="burger__item"><a href="#contact" class="burger__link">Contact</a></li>
          </ul>
        </nav>
      </div>
    </transition>
  </div><!-- /.burger -->
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
  .burger {
    display: none;
  }

  .burger__icon {
    border: none;
    display: block;
    height: 39px;
    position: relative;
    width: 39px;
    z-index: 3;
  }

  .burger__bar {
    background-color: #fff;
    display: block;
    height: 3px;
    left: 50%;
    position: absolute;
    transform: translateX(-50%);
    width: 20px;
  }

  .burger__bar-top {
    top: 10px;
  }

  .burger__bar-mid {
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .burger__bar-bottom {
    bottom: 10px;
  }

  .burger__bar.close {
    background-color: #fff;
  }

  .burger__bar-top.close {
    transform: translate(-50%, 10px) rotate(45deg);
    transition: transform .3s;
  }

  .burger__bar-mid.close {
    opacity: 0;
    transition: opacity .3s;
  }

  .burger__bar-bottom.close {
    transform: translate(-50%, -6px) rotate(-45deg);
    transition: transform .3s;
  }

  .burger__wrapper {
    height: 100vh;
    left: 0;
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 2;
  }

  .burger__menu {
    background-color: #282F35;
    height: 100%;
    width: 100%;
    z-index: 2;
  }

  .burger__menu .burger__list {
    display: block;
    left: 50%;
    list-style: none;
    position: absolute;
    text-align: center;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .burger__menu .burger__item {
    margin-bottom: 40px;
    margin-right: 0;
  }

  .burger__item {
    font-style: italic;
    font-weight: bold;
    line-height: 1.375;
    letter-spacing: 0.05em;
  }

  .burger__link {
    color: #fff;
  }

  /* アニメーション */
  .burger__menu-enter-active, .burger__menu-leave-active {
    transition: opacity 0.4s;
  }
  
  .burger__menu-enter, .burger__menu-leave-to {
    opacity: 0;
  }
  
  .burger__menu-leave, .burger__menu-enter-to{
    opacity: 1;
  }

  @media screen and (max-width: 414px) {
    .burger {
      display: block;
    }
  }
  
</style>
