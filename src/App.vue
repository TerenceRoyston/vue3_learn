<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import MyApp1 from "./components/MyApp1.vue";
import MyReactive1 from "@/components/MyReactive1.vue";
import MyRef1 from "@/components/MyRef1.vue";
import MyComputed1 from "@/components/MyComputed1.vue";
import MyWatch1 from "@/components/MyWatch1.vue";
import MyTempleteRef1 from "@/components/MyTempleteRef1.vue";



import {ref} from 'vue'
const count1 = ref(0)
const addCount1 = () => count1.value++
</script>



<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    addCount() {
      this.count++
    }
  }
}
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="Man ! You did it!" />
    </div>

<!--    <button @click="addCount" class="button">{{count}}</button>-->
    <button @click="addCount" >{{count}}</button>
    <button @click="addCount1" >{{count1}}</button>

  </header>

  <main>
    <TheWelcome />
    <MyApp1 />
    <MyReactive1 />
    <MyRef1 />
    <MyComputed1 />
    <MyWatch1 />
    <MyTempleteRef1 />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
