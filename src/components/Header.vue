<template>
  <header class="header">
    <div class="header__inner">
      <div class="header__logo"><a href="/" class="header__link">Cresta Design</a></div><!-- /.header__logo -->
      <nav class="header__nav">
        <ul class="header__list">
          <li class="header__item">
            <a href="#concept" class="header__link">Concept</a><!-- /.header__link -->
          </li><!-- /.header__item -->
          <li class="header__item">
            <a href="#service" class="header__link">Service</a><!-- /.header__link -->
          </li><!-- /.header__item -->
          <li class="header__item">
            <a href="#works" class="header__link">Works</a><!-- /.header__link -->
          </li><!-- /.header__item -->
          <li class="header__item">
            <a href="#contact" class="header__link">Contact</a><!-- /.header__link -->
          </li><!-- /.header__item -->
        </ul><!-- /.header__list -->
      </nav><!-- /.header__nav -->
      <Burger/>
    </div><!-- /.header__inner -->
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
  .header {
    font-style: italic;
    position: fixed;
    width: 100%;
  }

  .header__inner {
    padding: 19px 120px;
    display: flex;
    justify-content: space-between;
  }

  .header__logo {
    font-size: 1.625rem;
    font-weight: bold;
    line-height: 2.25rem;
  }

  .header__nav {
    display: flex;
    align-items: center;
  }

  .header__list {
    display: flex;
    list-style: none;
  }

  .header__item {
    margin-right: 30px;
    font-weight: bold;
    line-height: 1.375rem;
  }

  .header__item:last-child {
    margin-right: 0;
  }

  @media screen and (max-width: 414px) {

    .header__inner {
      padding: 19px 15px;
    }

    .header__list {
      display: none;
    }

  }

</style>
