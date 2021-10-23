<template>
  <div class="contact">
    <SubFirstView title="Contact" backgroundText="Contact Us"></SubFirstView>
    <Form/>
    <Button text="Submit"></Button>
  </div>
</template>

<script>
import SubFirstView from '../components/SubFirstView.vue' 
import Form from '../components/Form.vue' 
import Button from '../components/Button.vue' 

export default {
  name: 'Contact',
  components: {
    SubFirstView,
    Form,
    Button
  }
}
</script>

<style>
  .sbfv {
    margin-bottom: 100px;
  }

  .form {
    margin-bottom: 80px;
  }

  .btn {
    margin-bottom: 80px;
  }
</style>