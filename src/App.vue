<script setup lang="ts">
import { ref } from "vue";
import PageHome from "./views/PageHome.vue";
import PagePreStart from "./views/PagePreStart.vue";

export type Page = "home" | "pre-start" | "game" | "result";
const page = ref<Page>("home");
</script>

<template>
  <div class="container">
    <PageHome v-if="page === 'home'" @change-page="page = $event"></PageHome>
    <PagePreStart v-if="page === 'pre-start'"></PagePreStart>
  </div>

  <h1></h1>
</template>

<style scoped>
body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
}
</style>
