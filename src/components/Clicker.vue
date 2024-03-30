<template>
  <div>
    <Time @select-time="setTime"></Time>
    <div v-if="time">
      <p>Время: {{ time }} секунд</p>
      <button @click="startTest">Начать тест</button>
    </div>
  </div>
</template>

<script>

</script>
