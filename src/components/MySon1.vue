<script setup>
/*defineProps({
  message: String
})*/

const props = defineProps({
  message: String,
  count: Number
})

console.log(props)

</script>

<template>
<div>
  <h1>son component 1</h1>
  <h1>father component => {{message}} => {{count}}</h1>
</div>
</template>

<style scoped>

</style>