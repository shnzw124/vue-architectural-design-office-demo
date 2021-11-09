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
<style scoped>
  .Btn {
    display: inline-block;
    width: 235px;
    max-width: 100%;
    padding: 19px 10px 18px;
    background-color: #F7D43F;
    box-shadow: 0 0 6px #423d3b;
    color: #171717;
    font-weight: bold;
    font-size: 1.125rem;
    text-align: center;
    text-decoration: none;
    transition: .25s;
    border-radius: 50px;
    line-height: 1.875;
    letter-spacing: 0.05em;
  }

  .Btn:focus, .Btn:hover {
    background-color: #fff;
    color: #F7D43F;
  }
  
</style>
