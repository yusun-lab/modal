<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Giveaway</h1>
      <p>Grab your ninja swag for half price!</p>
    </Modal>
  </div>

  <div v-if="showModalTwo">
    <ModalTwo theme="fresh" @close="toggleModalTwo">
      <template v-slot:vart>
        <a href="#">turn left</a>
        <a href="#">turn right</a>
      </template>
    </ModalTwo>
  </div>

  <button @click.alt="toggleModal">Open modal (alt)</button>

  <p>Hejdå</p>

  <button @click.shift="toggleModalTwo">Open modal (shift)</button>
</template>

<script setup lang="ts">
/*  challenge:
- create an extra button to open a different modal
- use the same modal component but pass in a different template (slot)
- use a different method (e. g. toggleModalTwo) and data (e. g. showModalTwo)
*/
import Modal from "./components/Modal.vue";
import ModalTwo from "./components/ModalTwo.vue";
import { ref } from "vue";

const title = ref("My first Vue 3 app:)");
const showModal = ref(false);
const showModalTwo = ref(false);

const toggleModal = () => {
  showModal.value = !showModal.value;
};
const toggleModalTwo = () => {
  showModalTwo.value = !showModalTwo.value;
};
</script>

<style>
#app {
  /* this app div right here is not actually inside this component, it's in the public\index.html\<div id="app"></div> */
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
