<template>
  <h1>{{ title }}</h1>
  <Modal />
</template>

<script setup lang="ts">
import Modal from "./components/Modal.vue";
import { useTemplateRef } from "vue";

const title = "My first Vue 3 app";
</script>

<!-- <style scoped> scoped <style> won't apply its style to anything outside this component-->
<style>
#app {
  /* this app divv right here is not actully inside this component, it's in the public\index.html\<div id="app"></div> */
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
