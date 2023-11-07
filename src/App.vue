<template>
  <div id="app">
    <MySlider />
  </div>
</template>

<script>

import MySlider from "./components/MySlider.vue";

export default {
  components: {
    MySlider,
  },
};

</script>

<style>

*::selection {
  background: transparent;
}

body {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  font-family: sans-serif;
}

input {
  border: none;
  border-bottom: 2px solid #ddd;
  outline: none;
  font-size: 20px;
  padding: 10px 15px;
}

button {
  padding: 7px 13px;
  border: none;
  font-size: 20px;
  background: #41b883;
  box-shadow: 0 0 3px #888;
  color: #fff;
  border-radius: 5px;
}

p {
  font-size: 17px;
}

</style>