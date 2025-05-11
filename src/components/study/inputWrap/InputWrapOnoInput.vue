<!--<script setup lang="ts">-->
<!--const emit = defineEmits([-->
<!--  'update:modelValue'-->
<!--]);-->
<!--const props = defineProps([-->
<!--  'modelValue',-->
<!--])-->

<!--const onInput = (event) => {-->
<!--  emit('update:modelValue', event.target.value)-->
<!--}-->

<!--</script>-->

<!--<template>-->
<!--  <input type="text" :value="props.modelValue" @input="onInput" placeholder="text"/>-->
<!--</template>-->

<!--<style scoped>-->

<!--</style>-->

22222222
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
  <input :value="props.value" @input="onInput" placeholder="text"/>
</template>

<style scoped>

</style>