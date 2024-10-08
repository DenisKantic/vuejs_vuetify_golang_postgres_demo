<template>
  <div class="test-container">
    <input v-model="message" placeholder="Type something..." />
    <p class="centered-message">You typed: {{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Test",
    };
  },
};
</script>

<style scoped>
.test-container {
  background-color: green;
  display: flex;
  min-height: 100svh;
  flex-direction: column; /* Stack elements vertically */
  align-items: center; /* Center align items horizontally */
  justify-content: center; /* Center align items vertically */
}

.centered-message {
  color: red;
  margin-top: 16px; /* Add some space above the message */
}
</style>
