<template>
  <h1>{{ title }}</h1>
  <Modal :header="header" :text="text" theme="sale" />
  <!-- this is how we pass data as props into components which a: makes them more reusable, b: makes them more customizable, and c: allow us to have a single source of truth when it comes to our data -->
</template>

<script setup lang="ts">
import Modal from "./components/Modal.vue";
import { ref } from "vue";

const title = ref("My first Vue 3 app!");
const header = ref("Sign up for the Giveaway!");
const text = ref("Grab your ninja swag for half price!");
</script>

<!-- <style scoped> scoped <style> won't apply its style to anything outside this component-->
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
