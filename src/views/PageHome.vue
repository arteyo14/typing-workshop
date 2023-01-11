<template>
  <h1>Welcome to my game</h1>
  <button @click="emit('change-page', 'game')">Start Game</button>
</template>

<script setup lang="ts">
import { Page } from "../App.vue";
const emit = defineEmits<{
  (event: "change-page", name: Page): void;
}>();
</script>

<style scoped>
.container {
  padding: 1rem;
}

button {
  padding: 0.5rem 1rem;
  font-size: 1.1rem;
}

.center {
  text-align: center;
}
</style>
