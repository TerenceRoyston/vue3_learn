<script setup>
import MySon2 from './MySon2.vue'
const handleMsg = (msg) => {
  console.log(msg)
}
</script>

<template>
  <div>
    <h1>MyFather2</h1>
    <MySon2 @sendMyMsg="handleMsg" />
  </div>
</template>

<style scoped>

</style>