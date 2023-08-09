<script setup>
defineProps({
  level: {
    type: String,
    required: true,
  },
});
const classes = {
  1: "text-4xl",
  2: "text-3xl",
  3: "text-2xl",
  4: "text-xl",
  5: "text-lg",
  6: "text-base",
};
</script>

<template>
  <component :is="`h${level}`" class="font-bold mb-4" :class="classes[level]">
    <slot />
  </component>
</template>
