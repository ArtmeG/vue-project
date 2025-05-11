<script setup lang="ts">
const emit = defineEmits([
  'update:modalValue'
]);
const props = defineProps([
  'modalValue',
]);
const onInput = (event) => {
  emit('update:modalValue', event.target.value)
}
</script>

<template>
  <input type="text" :value="props.modalValue" @input="onInput" placeholder="text"/>
</template>

<style scoped>

</style>
