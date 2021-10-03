<script setup lang="ts">
import Main from "@components/view/Main.vue";
</script>

<template>
  <Main />
</template>

<style>
@tailwind components;
@tailwind utilities;

body {
  @apply h-screen p-0 m-0 box-border;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

a {
  @apply no-underline text-current
}
</style>
