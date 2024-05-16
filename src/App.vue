<!-- App.vue -->
<template>
  <div class="app-container">
    <TextHeader />
    <div class="content">
      <Text :message="message" />
      <Button @emit-data="handleEmitData" />
      <SlotC>
        <template v-slot:header>
          <h2>Sajak Patah Hati</h2>
        </template>
        <template v-slot:default>
          Default slot content
        </template>
        <template v-slot:footer>
          <p>Wangi baunya indah, parasnya bagaikan bunga mawar yang tampak indah diluar tapi tidak dengan akarnya yang akan membawa sakit dan luka jika kita menyentuhnya.</p>
        </template>
      </SlotC>
    </div>
  </div>
</template>

<script>
import Text from './components/Text.vue';
import Button from './components/Button.vue';
import Emit from './components/Emit.vue';
import TextHeader from './components/TextHeader.vue';
import SlotC from './components/SlotC.vue';

export default {
  components: { Text, Button, Emit, TextHeader, SlotC },
  data() {
    return {
      message: '',
    };
  },
  methods: {
    handleEmitData(data) {
      this.message = data;
    },
  },
};
</script>

<style scoped>
.app-container {
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
}

.content {
  padding: 20px;
}

h1, h2 {
  color: #333;
  font-weight: bold;
  margin-bottom: 10px;
}

h2 {
  font-size: 18px;
}

p {
  font-size: 16px;
  color: #666;
  margin-bottom: 20px;
}
</style>
