<template>
  <div class="backdrop">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>{{ header }}</h1>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<!-- Vue 2 Options API: -->
<!-- <script>
export default {
  props: ["header", "text"],
};
</script> -->

<!-- Vue 3 -->
<script setup lang="ts">
const props = defineProps<{
  header: string | (string | number)[];
  text: string;
  theme: string;
}>();
</script>

<style>
/* <style scoped> */
.modal {
  width: 400px;
  padding: 20px;
  background: white;
  margin: 100px auto;
  border-radius: 10px;
}

.backdrop {
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}

.modal h1 {
  color: #03cfb4;
  border: none;
  padding: 0;
}

.modal p {
  font-style: normal;
}

.modal.sale {
  background: crimson;
  color: white;
}

.modal.sale h1 {
  color: white;
}
</style>
