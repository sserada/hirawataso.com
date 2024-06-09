8<template>
  <div id="scroll-down">
    <svg
      id="scroll-down-svg"
      xmlns="http://www.w3.org/2000/svg"
      width="64"
      height="64"
      viewBox="0 0 24 24"
      fill="none"
      stroke="currentColor"
      stroke-width="0.5"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <polyline points="6 9 12 15 18 9"></polyline>
    </svg>
  </div>
</template>

<script lang="ts" setup>
import { onMounted } from 'vue';
onMounted(() => {
  const svg = document.getElementById('scroll-down-svg');
  svg?.classList.add('scroll-animation');
});
</script>

<style scoped>
#scroll-down {
  display: flex;
  justify-content: center;
  align-items: center;
}

#scroll-down-svg {
  opacity: 0.5;
  animation: scroll-down 2s infinite;
}

@keyframes scroll-down {
  0% {
    transform: translateY(0);
    opacity: 0.2;
  }
  50% {
    transform: translateY(10px);
    opacity: 0.8;
  }
  100% {
    transform: translateY(0);
    opacity: 0.2;
  }
}
</style>

