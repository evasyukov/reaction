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
import Time from "./Time.vue"

export default {
  name: "Clicker",
  components: {
    Time,
  },
  data() {
    return {
      time: null,
      clicks: 0,
    }
  },
  methods: {
    setTime(time) {
      this.time = time
    },
    startTest() {
      this.clicks = 0
      this.timer = setInterval(() => {
        this.clicks++
      }, 1000)
      setTimeout(() => {
        clearInterval(this.timer)
        this.$emit("test-result", this.clicks)
      }, this.time * 1000)
    },
  },
}
</script>
