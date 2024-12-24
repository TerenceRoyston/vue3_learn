<script setup>
// no need to register son component
import SonCom from './MySon1.vue'
import {ref} from "vue";
const count =ref(100)
const addCount = () => {
  count.value++
}
</script>

<template>
  <div>
    <h1>father component 1</h1>
    <button @click="addCount">add count</button>

    <SonCom :count = "count" message="father message"/>
  </div>
</template>

<style scoped>

</style>