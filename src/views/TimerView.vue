<script lang="ts">
import { defineComponent } from 'vue'
import TimerPageView from '@/components/dashboard/timerPage/TimerPageView.vue'

export default defineComponent({
  name: 'TimerView',
  components: { TimerPageView },
})
</script>

<template>
  <TimerPageView />
</template>

<style scoped></style>
