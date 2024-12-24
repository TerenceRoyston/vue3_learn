<script setup>
import {provide, ref} from 'vue'
import MyInject1 from "@/components/MyInject1.vue";

// 传递静态数据
provide('provide-key', 'provide-value')

// 传递动态数据
const count = ref(0)
provide('ref-key', count)

// 传递方法
const addCount = ()=>{
  count.value++
}
provide('addCount-key', addCount)

</script>

<template>
  <h1>父组件provide 1</h1>

  <button @click="addCount">count+1</button>
  <MyInject1 />
</template>

<style scoped>

</style>