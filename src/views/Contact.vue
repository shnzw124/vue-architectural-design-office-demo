<template>
  <div class="Contact">
    <SubFirstView 
      class="Contact_Sbfv"
      title="Contact"
      backgroundText="Contact us">
    </SubFirstView>
    <Form class="Contact_Form"></Form>
    <Button 
      class="Contact_Btn"
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
  .Contact_Sbfv {
    margin-bottom: 100px;
  }

  .Contact_Form {
    margin-bottom: 80px;
  }

  .Contact_Btn {
    margin-bottom: 80px;
  }
</style>