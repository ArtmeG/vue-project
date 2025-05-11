<script setup lang="ts">

import DefaultLayoutHeader from "@/layout/DefaultLayoutHeader.vue";
import DefaultLayoutFooter from "@/layout/DefaultLayoutFooter.vue";

defineProps( {
  isVisibleFooter: {
    type: Boolean,
    default: true
  }
})

</script>

<template>
  <div>
    <DefaultLayoutHeader/>
    <main>
      <slot/>
    </main>
    <DefaultLayoutFooter v-if="isVisibleFooter" />
  </div>
</template>

<style scoped>

</style>