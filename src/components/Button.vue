<template>
  <a class="Btn" :href="url">{{ text }}</a><!-- /.button -->
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    url: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Btn {
    background-color: #f7d43f;
    border-radius: 50px;
    box-shadow: 0 0 6px #423d3b;
    color: #171717;
    display: inline-block;
    font-size: 1.125rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.875;
    max-width: 100%;
    padding: 19px 10px 18px;
    text-align: center;
    text-decoration: none;
    transition: .25s;
    width: 235px;
  }
  .Btn:focus,
  .Btn:hover {
    background-color: #fff;
    color: #f7d43f;
  }

</style>
