<template>
    <Clicker @test-result="showResult" />
    <Result v-if="result" :clicks="result" />
</template>

<script>
import Clicker from "./components/Clicker.vue"
import Result from "./components/Result.vue"

export default {
  name: "App",
  components: {
    Clicker,
    Result,
  },
  data() {
    return {
      result: null,
    }
  },
  methods: {
    showResult(clicks) {
      this.result = clicks
    },
  },
}
</script>

<style scoped></style>
