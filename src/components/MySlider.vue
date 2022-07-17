<template>
<div class="box"></div>
  <div class="slider">
    <div class="front"></div>
    <div class="back"></div>
    <div class="left"></div>
    <div class="right"></div>
  </div>
  <p />
  <button @click="LeftSide">left</button>
  <button @click="RightSide">right</button>
</template>

<script>
export default {
  data() {
    return {
      Change: 0,
    };
  },
  methods: {
    LeftSide() {
      this.Change += 90;
      document.querySelector(
        ".slider"
      ).style.transform = `perspective(800px) rotateX(270deg) rotate(${this.Change}deg) translateZ(-150px)`;
    },
    RightSide() {
      this.Change -= 90;
      document.querySelector(
        ".slider"
      ).style.transform = `perspective(800px) rotateX(270deg) rotate(${this.Change}deg) translateZ(-150px)`;
    },
  },
};
</script>

<style scoped>
body {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  font-family: sans-serif;
}
.box {
  width: 100%;
  height: 100vh;
  position: absolute;
  left: 0;
  top: 0;
  box-shadow: inset 0 0 100px #111;
}
.slider {
  width: 400px;
  height: 400px;
  background: transparent;
  transform: perspective(800px) rotateX(270deg) rotate(0deg)
    translateZ(-150px);
  transform-style: preserve-3d;
  transition: 500ms;
}
.front,
.back,
.left,
.right {
  width: 100%;
  height: 300px;
  position: absolute;
  box-shadow: 0 0 5px #ccc, inset 0 0 10px #ddd;
  border-radius: 10px;
}
.front {
  transform: rotateX(90deg) translate3d(0, 150px, 150px);
  background: url("../assets/img/nature.jpg") 50% no-repeat;
  background-size: 150%;
}
.back {
  transform: rotateX(90deg) translate3d(0, 150px, -250px);
  background: url("../assets/img/beach.jpg") 50% no-repeat;
  background-size: 150%;
}
.left {
  transform: rotateX(90deg) rotateY(90deg) translate3d(50px, 150px, -200px);
  background: url("../assets/img/forest.jpg") 50% no-repeat;
  background-size: 150%;
}

.right {
  transform: rotateX(90deg) rotateY(90deg) translate3d(50px, 150px, 200px);
  background: url("../assets/img/mountain.jpg") 50% no-repeat;
  background-size: 150%;
}
button {
  text-transform: uppercase;
  text-shadow: 0 0 5px #666;
  transition: 100ms;
  position: relative;
  left: 100px;
  margin-left: 10px;
}
button:active {
  text-shadow: 0 0 1px #666;
}
img {
  width: 50%;
  z-index: 1000;
  position: absolute;
  left: 160px;
  top: 24%;
  /* box-shadow: 0 0 5px #ddd; */
}
</style> 