<template>
  <input placeholder="Write Something..." v-model="input" />
  <p>Your Text: {{ input }}</p>
</template>

<script>
export default {
  data() {
    return {
      input: "",
    };
  },
};
</script>

<style scoped>

input {
  width: 200px;
  font-size: 20px;
  padding: 10px 15px;
  border: none;
  border-bottom: 2px #ddd solid;
  outline: none;
}
</style>
