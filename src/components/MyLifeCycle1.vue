<script setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated } from 'vue'

// before mounted
onMounted(() => {
  console.log('onMounted')
})

// 支持多个
onMounted(() => {
  console.log('onMounted1')
})


</script>

<template>

</template>

<style scoped>

</style>