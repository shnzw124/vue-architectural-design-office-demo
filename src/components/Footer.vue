<template>
  <footer class="Footer">
    <div class="Footer_Inner">
      <p class="Footer_Text">©︎cresta.design all rights reserved</p><!-- /.Footer_Text -->
    </div><!-- /.Footer_Inner -->
  </footer><!-- /.Footer -->
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Footer_Inner {
    padding-bottom: 30px;
    padding-top: 30px;
  }
  .Footer_Text {
    color: #282f35;
    font-size: 14px;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 2.14286;
    text-align: center;
  }

</style>
