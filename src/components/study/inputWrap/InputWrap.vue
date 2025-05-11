<script setup lang="ts">
import {ref} from "vue";
import InputWrapOnoInput from "@/components/study/inputWrap/InputWrapOnoInput.vue";

const text = ref('');

</script>

<template>
  <div class="todo-wrapper">
    // 1
    <input class="todo-wrapper-input"  :value="text" @input="text=$event.target.value.trim()" />
    // 2
    <input class="todo-wrapper-input" v-model.trim="text" />

    <!--  // 3-->
    <!--  <InputWrapOnoInput v-model="text"/>-->
    // 4
    <InputWrapOnoInput v-model:value.trim="text"/>

    <h1>
      {{text}}
    </h1>
  </div>


</template>

<style scoped>
.todo-wrapper {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.todo-wrapper-input {
  border: 1px solid green;
  border-radius: 5px;
  padding: 5px;
}



</style>