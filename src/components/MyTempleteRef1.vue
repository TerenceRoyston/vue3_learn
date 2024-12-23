<script setup>
import { ref , onMounted} from 'vue'
import MyTestTemplateRef1 from "@/components/MyTestTemplateRef1.vue";
const h1ref = ref(null)
const testRef1 = ref(null)

onMounted(() => {
  console.log(h1ref.value)
  console.log(testRef1.value)
})

</script>

<template>
  <div>
    <h1 ref="h1ref">Hello World</h1>
    <MyTestTemplateRef1 ref="testRef1"/>
    <my-test-template-ref1/>
  </div>
</template>

<style scoped>

</style>