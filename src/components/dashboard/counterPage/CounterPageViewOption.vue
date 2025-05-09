<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CounterPageViewOption',
  data () {
    return {
      count: 0
    }
  },
  methods: {
    increment () {
      this.count++;
    }
  },
  watch: {
    count (newValue, oldValue) {
      console.log('count changed', newValue, oldValue);
    }
  },
  computed: {
    doubleCount () {
      return this.count * 2;
    }
  },
})
</script>

<template>
  <h1>Counter: {{ count }}</h1>
</template>

<style scoped>

</style>
