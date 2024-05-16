<!-- Text.vue -->
<template>
  <div>
    {{ message }}
  </div>
</template>

<script>
export default {
  props: {
    message: String,
  },
};
</script>

<style scoped>
div {
  font-size: 18px;
  font-weight: bold;
  color: #333;
  margin-bottom: 20px;
}
</style>
