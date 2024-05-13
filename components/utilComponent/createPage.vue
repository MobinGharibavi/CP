<template>
  <section class="flex flex-col bg-white p-6 gap-5">
    <div class="flex itemsc-center gap-3">
      <img src="/icon/flash-right.svg" alt="..." />

      <h5 class="text-[1.625rem] font-semibold">{{ title }}</h5>
    </div>

    <slot />
  </section>
</template>

<script setup>
const { title } = defineProps({
  title: String,
});
</script>
