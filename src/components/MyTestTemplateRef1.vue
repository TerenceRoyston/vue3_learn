<script setup>
import {ref} from 'vue'
const name = ref('test_ref1')

// 暴露组件内部的属性和方法
defineExpose({
  name
})
</script>

<template>
<div>
  <h1>MyTestTemplateRef1!!</h1>
</div>
</template>

<style scoped>

</style>