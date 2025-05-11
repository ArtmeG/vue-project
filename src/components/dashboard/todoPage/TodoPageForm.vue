<script setup lang="ts">

import {ref} from "vue";
import Checkbox from "@/components/base/checkbox/Checkbox.vue";
import Input from "@/components/base/input/Input.vue";

const form = ref({
  checkbox: false,
  text: ''
});

</script>

<template>
  <Checkbox v-model:value="form.checkbox"/>
  <Input :modal-value="form.text" @update:modalValue="(value) => (form.text = value)" />

  {{form.checkbox}}

</template>

<style scoped>

</style>