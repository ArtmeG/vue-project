<script setup lang="ts">
const emit = defineEmits([
  'update:value'
]);
const props = defineProps([
  'value',
]);
const onInput = (event) => {
  emit('update:value', event.target.value)
}
</script>

<template>
  <input type="checkbox" :value="props.value" @input="onInput" placeholder="text"/>
</template>

<style scoped>

</style>
