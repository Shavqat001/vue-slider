<template>
  <button @click="ShowHide">Show | Hide</button>
  <p v-if="toggle">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Facilis quos nam
    sequi et autem velit voluptates ipsa! Doloremque, reprehenderit veritatis?
    Architecto, fugit. Beatae ratione dicta nam ipsam repellendus eaque
    corporis.
    <img src="../assets/logo.png" alt="">
  </p>
</template>

<script>
export default {
  data() {
    return {
      toggle: true,
    };
  },
  methods: {
    ShowHide() {
      this.toggle = !this.toggle;
    },
  },
};
</script>

<style>
</style>