<template>
  <h1>Hello, I'm Learning Vue</h1>
  <h4>Vue is Fun</h4>
  <Form placeholder="Enter name" />
  <div v-if="showModal">
    <Modal :theme="theme" @close="handleClick">
      <template v-slot:links>
        <a href="#">Learn more</a>
      </template>
      <template v-slot:socials>
        <p>Contact us (LinkedIn)</p>
      </template>
      <h1>Hey, I'm a Modal</h1>
      <p>Modals are pop-ups used to pass an information and are triggered by an event</p>
    </Modal>
  </div>
  <button class="btn" @click="handleClick">Show Modal</button>

  <div v-show="showModal2">
    <Modal theme="dark" @close="handleClick2">
      <h1>Hey, I'm the Second Modal</h1>
      <p>Modals can be used to collect form data quickly also, its fun learning vue</p>

      <template v-slot:socials>
        <p>Click here to <a href="#">Visit my Website</a></p>
      </template>
    </Modal>
  </div>

  <button @click="handleClick2">Show Modal Two</button>
</template>

<script>
import Form from "./components/Form.vue";
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      theme: "light",
      showModal: false,
      showModal2: false,
    };
  },
  methods: {
    handleClick() {
      this.showModal = !this.showModal;
    },

    handleClick2() {
      this.showModal2 = !this.showModal2;
    },
  },
  components: { Form, Modal },
};
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
