<template>
  <Test />
</template>

<script>
console.log("Test");
import Test from "./Test.vue";

export default {
  components: {
    Test,
  },

  mounted() {
    console.log("component mounted");
  },
};
</script>
