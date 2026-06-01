<template>
  <h1> Hello, I'm Learning Vue</h1>
  <h4>Vue is Fun</h4>
  <Form placeholder="Enter name"/>
  <Form placeholder="Enter age"/>
  <Modal heading="Hey, I'm a Modal" text="Modals are pop-ups used to pass an information and are triggered by an event"/>
</template>

<script>
import Form from './components/Form.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  
  components: {
     Form, Modal
  }
}
</script> 

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
