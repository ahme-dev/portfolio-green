<script setup lang="ts">
  import { computed, ref } from "vue";
  import { useMouseInElement } from "@vueuse/core";
  const target = ref(null);
  const { elementX, elementY, isOutside, elementHeight, elementWidth } =
    useMouseInElement(target);

  const cardTransform = computed(() => {
    const MAXROT = 18;

    const rX = (
      MAXROT / 2 -
      (elementY.value / elementHeight.value) * MAXROT
    ).toFixed(2);
    const rY = (
      (elementX.value / elementWidth.value) * MAXROT -
      MAXROT / 2
    ).toFixed(2);

    return isOutside.value
      ? ""
      : `perspective(${
          elementWidth.value * 3
        }px) rotateX(${rX}deg) rotateY(${rY}deg)`;
  });
</script>

<template>
  <p
    class="bg-gray-500 text-gray-800 bg-opacity-20 p-4 text-2xl w-1/1 hover:(shadow-lg shadow-emerald-300 cursor-pointer)"
    ref="target"
  >
    <slot></slot>
  </p>
</template>

<style scoped>
  p {
    transform: v-bind(cardTransform);
    transition: transform 0.2s;
  }
  *::selection {
    @apply bg-emerald-300;
  }
</style>
