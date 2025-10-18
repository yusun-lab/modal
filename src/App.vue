<template>
  <h1>{{ title }}</h1>
</template>

<script lang="ts">
// import { Options, Vue } from "vue-class-component";
export default {
  name: "App",
  data() {
    return {
      title: "My first Vue 3 App",
    };
  },
};
// export default class App extends Vue {}
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
