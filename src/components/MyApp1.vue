<script setup>
const message = 'my message ok1'
const logMessage = () => console.log(message)
const logMessage1 = () => window.alert(message)
</script>

<script>
export default {
  setup() {
    const message = 'my message ok'
    const logMessage = () => console.log(message)
    const logMessage1 = () => window.alert(message)
    return {
      message,
      logMessage,
      logMessage1
    }
  }
}

</script>

<template>

  <div>{{message}}</div>
  <button @click="logMessage">log message</button>
  <button @click="logMessage1">log message1</button>

</template>

<style scoped>

</style>