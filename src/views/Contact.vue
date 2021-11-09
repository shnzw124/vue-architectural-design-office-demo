<template>
  <div class="contact">
    <SubFirstView 
      class="contact__sbfv"
      title="Contact"
      backgroundText="Contact us">
    </SubFirstView>
    <Form class="contact__form"></Form>
    <Button 
      class="contact__btn"
      text="Submit">
    </Button>
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
  .contact__sbfv {
    margin-bottom: 100px;
  }

  .contact__form {
    margin-bottom: 80px;
  }

  .contact__btn {
    margin-bottom: 80px;
  }
</style>