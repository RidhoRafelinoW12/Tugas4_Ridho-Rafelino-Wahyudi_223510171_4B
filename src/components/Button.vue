<!-- Button.vue -->
<template>
  <button @click="$emit('emit-data', 'Jika aku disuruh melukis, aku akan melukis sosok gadis. Jika aku disuruh melukis tentang gadis itu, aku akan mematahkan pena-ku.')">Click me!</button>
</template>

<script>
export default {
  // No need for any data or methods here
};
</script>

<style scoped>
button {
  background-color: #4CAF50;
  color: #fff;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  background-color: #3e8e41;
}
</style>
