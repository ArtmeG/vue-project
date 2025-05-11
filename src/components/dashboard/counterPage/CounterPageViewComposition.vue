<script setup lang="ts">
import {computed,  ref, watch} from "vue";

  const count = ref(0)

  const increment = () => {
    count.value++;
  }

  const doubleCount = computed(() => {
    return count.value * 2;
  })

// watch(
//     ( ) => { return count},
//     (newValue, oldValue) => {
//   console.log('count changed', newValue, oldValue);
// }, {immediate: true}
// )

  watch(count, (newValue, oldValue) => {
    console.log('count changed', newValue, oldValue);
  })

</script>

<template>
  <h1>Counter: {{ count }}</h1>
  <h1>doubleCount: {{ doubleCount }}</h1>
  <button @click="increment">Increment</button>
</template>

<style scoped>

</style>
