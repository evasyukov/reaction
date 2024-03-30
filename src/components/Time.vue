<template>
  <div>
    <button @click="$emit('select-time', 10)">10 секунд</button>
    <button @click="$emit('select-time', 30)">30 секунд</button>
    <button @click="$emit('select-time', 60)">60 секунд</button>
  </div>
</template>

<script>
export default {
  name: "Time",
}
</script>

<style>
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
</style>
