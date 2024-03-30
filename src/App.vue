<template>
  <div class="menu">
    <button>10 sec</button>
    <button>30 sec</button>
    <button>60 sec</button>
  </div>
  <div id="click" class="reaction"></div>
</template>

<script>
export default {
  components: {},
}
</script>

<style scoped>
.main {
  display: flex;
}
button {
  width: 100px;
  height: 100px;
  margin: 10px;
  border: 0;
  cursor: pointer;
  background: rgba(255, 255, 255, 0.4);
  backdrop-filter: blur(100px);
  border-radius: 50%;
}
button:active {
  background: #e30a0a;
  transition: 0.3s;
}
.reaction {
  width: 200px;
  height: 200px;
  background-color: aqua;
}
</style>
