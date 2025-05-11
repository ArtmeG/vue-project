<script setup lang="ts">
import {RouterView, useRoute} from 'vue-router'
import DefaultLayout from "@/layout/DefaultLayout.vue";
import {computed} from "vue";

const route = useRoute()

console.log('----------', route.meta)

const isVisibleFooter = computed(() => {
  console.log('----------', route.meta.isVisibleFooter)
  return route.meta.isVisibleFooter;
});

</script>

<template>
  <DefaultLayout :is-visible-footer="isVisibleFooter" >
    <RouterView />
  </DefaultLayout>
</template>