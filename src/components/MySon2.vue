<script setup>
const emit = defineEmits(['sendMyMsg'])
const sendMsg = () => {
  emit('sendMyMsg', 'it is son2')
}
</script>

<template>
<div>
  <h1>MySon2</h1>
  <button @click="sendMsg">send</button>
</div>
</template>

<style scoped>

</style>