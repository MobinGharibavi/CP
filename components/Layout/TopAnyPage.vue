<template>
  <div class="h-[5.5rem] w-full flex items-center justify-between px-8 shadow">
    <h2 class="text-[1.75rem] font-bold">
      {{ title }}
    </h2>

    <slot />
  </div>
</template>

<script setup>
const { title } = defineProps({
  title: String,
});
</script>
