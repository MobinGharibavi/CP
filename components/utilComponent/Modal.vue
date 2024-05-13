<template>
  <Transition name="modal-animation">
    <div
      class="flex justify-center z-50 items-center h-screen w-screen fixed top-0 left-0 bg-black/50"
      v-show="modalActive"
      @click.self="close"
    >
      <Transition name="modal-animation-inner">
        <div
          :class="{
            '!w-[34.5rem]': props.size == 'xs',
            'pt-12': !props.notShowTop,
          }"
          class="relative w-[46.5rem] shadow bg-gray-100 rounded-xl overflow-hidden"
          v-show="modalActive"
        >
          <!-- icon -->
          <div
            v-if="!props.notShowTop"
            class="absolute top-4 flex items-center gap-5 right-4 text-xl cursor-pointer transition-all hover:transition-all duration-500"
          >
            <img @click="close" src="/icon/close.svg" alt="" />
            <span :class="{ 'font-bold': props.boldTitle }">{{
              props.title
            }}</span>
          </div>
          <!-- modal content -->
          <slot />
        </div>
      </Transition>
    </div>
  </Transition>
</template>

<script setup>
const props = defineProps([
  "modalActive",
  "title",
  "size",
  "notShowTop",
  "boldTitle",
]);
const emit = defineEmits(["close"]);
const close = () => {
  emit("close");
  document.querySelector("body").classList.remove("overflow-hidden");
};
</script>

<style scoped>
.modal-animation-enter-active,
.modal-animation-leave-active {
  transition: opacity 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02);
}

.modal-animation-enter-from,
.modal-animation-leave-to {
  opacity: 0;
}

.modal-animation-inner-enter-active {
  transition: all 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02) 0.15s;
}
.modal-animation-inner-leave-active {
  transition: all 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02);
}
.modal-animation-inner-enter-from {
  opacity: 0;
  transform: scale(0.8);
}
.modal-animation-inner-leave-to {
  transform: scale(0.8);
}
</style>
