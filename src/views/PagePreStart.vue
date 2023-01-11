<template>
  <h1>Game Start in {{ countDown }}</h1>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";

const countDown = ref(3);

onMounted(() => {
  setInterval(() => {
    countDown.value--;
  }, 1000);
});
</script>

<style scoped></style>
