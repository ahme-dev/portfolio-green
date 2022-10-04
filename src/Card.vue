<script setup lang="ts">
  import { computed, ref } from "vue";
  import { useMouseInElement } from "@vueuse/core";
  const target = ref(null);
  const { elementX, elementY, isOutside, elementHeight, elementWidth } =
    useMouseInElement(null);

  const cardTrasform = computed(() => {
    const MAXROT = 8;

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
      : `perspective(${elementWidth.value}px) rotateX(${rX}deg) rotateY(${rY}deg)`;
  });
</script>

<template>
  <p
    class="bg-gray-500 text-gray-800 bg-opacity-20 p-4 text-2xl hover:(shadow-lg shadow-emerald-300 cursor-pointer)"
    :style="{
      transform: cardTrasform,
      transition: 'transform 0.2s ease-in-out',
    }"
  >
    <slot></slot>
  </p>
</template>
