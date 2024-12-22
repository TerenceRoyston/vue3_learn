<script setup>
import {ref} from 'vue'
const count = ref(1)
const setCount = ()=>{
  // 必须用.value 才能修改值
  count.value = 2
}
</script>

<template>
  <br>
<button @click="count++">{{count}}</button>
  <br>

</template>

<style scoped>

</style>