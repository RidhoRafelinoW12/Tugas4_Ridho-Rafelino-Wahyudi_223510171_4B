<!-- SlotC.vue -->
<template>
  <div>
    <slot name="header"></slot>
    <slot name="default"></slot>
    <slot name="footer"></slot>
  </div>
</template>

<script>
export default {
  // No need for any data or methods here
};
</script>

<style scoped>
div {
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  background-color: #f7f7f7;
}

h2 {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

p {
  font-size: 16px;
  color: #666;
  margin-bottom: 20px;
}
</style>
