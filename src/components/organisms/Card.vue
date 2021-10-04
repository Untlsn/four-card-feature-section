<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: 'Card',
  props: {
    barColor: {
      type: String,
      default: 'transparent'
    },
    title: {
      type: String,
    },
    text: {
      type: String,
    },
    imgSrc: {
      type: String,
      default: '',
    }
  },
})
</script>

<template>
  <div
      :style="{ 'border-top-color': barColor }"
      class="rounded bg-white shadow-2xl grid-area border-solid border-0 border-t-4
      pl-6 pr-2 relative cursor-pointer hover-scale h-64 mb-6 lg:h-auto lg:mb-0"
  >
    <h3 class="capitalize text-gray-900">{{ title }}</h3>
    <p class="text-gray-400">{{ text }}</p>
    <img :src="imgSrc" alt="" class="absolute bottom-4 right-4 h-[30%]">
  </div>
</template>

<style scoped>
.grid-area {
  --area: '';
  grid-area: var(--area);
}
.hover-scale {
  transition: transform .3s;
}
.hover-scale:hover {
  transform: scale(1.05);
}
</style>