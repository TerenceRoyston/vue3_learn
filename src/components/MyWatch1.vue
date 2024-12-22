<script setup>
import {ref} from 'vue'
import {watch} from 'vue'

const count = ref(0)
const name = ref('x11')
const state = ref({score: 0,age: 18})

const addCount = () => count.value++
const addName = () => name.value += '1'
const addScore = () => state.value.score++
const addAge = () => state.value.age++


// watch中的ref不需要加.value
// 监听单个数据源
watch(count, (newValue, oldValue) => {
  console.log('count的值被修改了', newValue, oldValue)
}, {immediate: true})
//immediate 立即执行回调

// deep 监听对象内部属性的变化
watch(
    state,
    (newValue, oldValue) => {
      console.log('state的值被修改了', newValue, oldValue)
    },
    {deep: true}
)

// 精准监听对象内部某个属性的变化 deep有性能问题，所以不建议使用
watch(
    () => state.value.age,
    () => {
      console.log('state.age的值被修改了', state.value.age)
    }
)

// 监听多个数据源
watch([count, name], ([newCount, newName], [oldCount, oldName]) => {
  console.log('count和name的值被修改了', newCount, oldCount, newName, oldName)
})
</script>

<template>
  <button @click="addCount">{{ count }}</button>
  <br>
  <button @click="addName">{{ name }}</button>
  <br>
  <button @click="addScore">{{ state.score }}</button>
  <br>
  <button @click="addAge">{{ state.age }}</button>
  <br>
</template>

<style scoped>

</style>