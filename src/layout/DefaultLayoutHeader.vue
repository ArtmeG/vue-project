<script setup lang="ts">

import {RouterLink} from "vue-router";
</script>

<template>
  <header class="header">
    <RouterLink  to="/">Logo</RouterLink>

    <nav class="header-nav">
      <RouterLink class="header-nav-item"  to="/">Home</RouterLink>
      <RouterLink class="header-nav-item" to="/about">About</RouterLink>
      <RouterLink class="header-nav-item" to="/counter">Counter</RouterLink>
      <RouterLink class="header-nav-item header-nav-item--red" to="/timer">Timer</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.header-nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.header-nav-item {
  font-size: 1.2rem;
  background: green;
}

.header-nav-item--red {
  background: red;
}
</style>