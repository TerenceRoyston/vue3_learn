<script setup>

import { inject } from 'vue'
const msg = inject('provide-key')
const injectCount = inject('ref-key')
// 接收方法
const addCount = inject('addCount-key')
</script>

<template>
  <h1>子组件inject 1</h1>
  <h1>子组件接收静态数据 => {{ msg }}</h1>
<button @click="addCount">子组件调用方法</button>
  <h1>子组件接收响应对象 => {{ injectCount }}</h1>

</template>

<style scoped>

</style>