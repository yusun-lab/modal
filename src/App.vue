<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">click me</button>
</template>

<script setup lang="ts">
// Applicable to vue3.4 and below:
// import { ref } from "vue";
// const title = ref("My first Vue 3 app");
// const name = ref<HTMLInputElement | null>(null);

// Applicable to vue3.5 and above:
import { useTemplateRef } from "vue";

const title = "My first Vue 3 app";
const name = useTemplateRef<HTMLInputElement>("name");

const handleClick = () => {
  console.log(name.value); // directly access the ref object: <input type="text">
  console.log(name.value?.value); // get the input field's value (optional chaining prevents null errors)

  name.value?.classList.add("active");
  name.value?.focus();
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

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
