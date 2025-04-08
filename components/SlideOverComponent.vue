<template>
  <Transition
    enter-active-class="transition ease-in-out duration-300 transform"
    enter-from-class="translate-x-[-100%]"
    enter-to-class="translate-x-0"
    leave-active-class="transition ease-in-out duration-250 transform"
    leave-from-class="translate-x-0"
    leave-to-class="translate-x-[-100%]"
  >
    <div
      class="w-[80%] h-screen sm:max-w-[450px] fixed top-0 left-0 z-[101] bg-white shadow-lg flex flex-col"
      v-show="props.isVisible"
    >
      <div>
        <!-- Header -->
        <div class="px-4 py-6">
          <div class="flex items-center justify-between">
            <h2 class="text-base font-semibold leading-6 text-gray-900">
              <slot name="title">Panel Title</slot>
            </h2>
            <div class="ml-3 flex h-7 items-center">
              <button
                type="button"
                class="rounded-md bg-white text-secondary hover:cursor-pointer focus:outline-none focus:ring-2 focus:ring-primary"
                @click="close"
              >
                <span class="sr-only">Close panel</span>
                <svg
                  class="h-6 w-6"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M6 18L18 6M6 6l12 12"
                  />
                </svg>
              </button>
            </div>
          </div>
        </div>
        <!-- Content -->
        <div class="relative flex-1 px-4 py-6 sm:px-6">
          <slot name="content"></slot>
        </div>
      </div>
    </div>
  </Transition>

  <Transition
    enter-active-class="transition-opacity ease-linear duration-300"
    enter-from-class="opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="transition-opacity ease-linear duration-250"
    leave-from-class="opacity-100"
    leave-to-class="opacity-0"
  >
    <div
      class="overlay fixed top-0 left-0 w-full h-full z-[100] bg-black/65"
      v-show="props.isVisible"
      @click="close"
    ></div>
  </Transition>
</template>

<script setup>
import { ref, defineEmits, defineProps, defineExpose } from "vue";

const props = defineProps({
  isVisible: {
    type: Boolean,
    default: false,
  },
});

const emit = defineEmits(["close"]);

const close = () => {
  emit("close");
};

defineExpose({
  close,
});
</script>

<style scoped></style>
