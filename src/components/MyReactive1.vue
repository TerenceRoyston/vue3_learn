<script setup>
import {reactive} from 'vue'

const state = reactive({
  count: 0
})
const addCount = () => state.count++
</script>

<template>
  <br>
  <div>
    <button @click="addCount">{{ state.count }}</button>
  </div>
  <br>
</template>

<style scoped>

</style>