<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'TimerPageView',
  data() {
    return {
      currentTime: new Date(),
    }
  },
  methods: {
    updateTime() {
      setInterval(() => {
        this.currentTime = new Date()
      }, 1000)
    },
  },
  watch: {
    getSeconds(time) {
      if (time == 0) {
        console.log('New minute started');
      }
    }
  },
  computed: {
    formatDate() {
      return this.currentTime.toLocaleTimeString();
    },
    getSeconds() {
      return this.currentTime.getSeconds();
    }
  },
  created() {
    this.updateTime();
  },
})
</script>

<template>
  <div>Current time: {{ formatDate }}</div>
</template>

<style scoped></style>
// date-fns
