<script setup lang="ts">
import Main from "@components/view/Main.vue";
</script>

<template>
  <Main />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;400;700&display=swap');

@tailwind components;
@tailwind utilities;

body {
  @apply h-screen p-0 m-0 box-border;
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
}

a {
  @apply no-underline text-current
}
</style>
