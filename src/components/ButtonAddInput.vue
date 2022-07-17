<template>
  <input type="search" size="30" v-model="input" />
  <p />
  <button @click="add">Add</button>
  <p>Your message: {{ message }}</p>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      message: "",
    };
  },
  methods: {
    add() {
      this.message = this.input;
    },
  },
};
</script>

<style scoped>

</style>
