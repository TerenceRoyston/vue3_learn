<script setup>
import {ref} from 'vue'
import {computed} from 'vue'

const list = ref([1, 2, 3, 4, 5])
const computedList = computed(() => {
  return list.value.map(item => item * 2)
})
// 测试计算属性是否跟着变化
setTimeout(() => {list.value.push(6,7)}, 2000)

</script>

<template>
  <div>
    原始数组 - {{list}}
  </div>
  <div>
    计算后的数组 - {{computedList}}
  </div>
</template>

<style scoped>

</style>