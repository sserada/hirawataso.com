<template>
  <div id="scroll-down">
    <svg
      id="scroll-down-svg"
      xmlns="http://www.w3.org/2000/svg"
      width="64"
      height="64"
      viewBox="0 0 100 100"
      fill="none"
      stroke="currentColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <circle cx="50" cy="50" r="45"></circle>
      <line x1="50" y1="30" x2="50" y2="70"></line>
      <polyline points="35 55 50 70 65 55"></polyline>
    </svg>
  </div>
</template>

<script lang="ts" setup>
import { onMounted } from 'vue';
import anime from 'animejs/lib/anime.es.js';

onMounted(() => {
  anime({
    targets: '#scroll-down-svg line, #scroll-down-svg polyline',
    strokeDashoffset: [anime.setDashoffset, 0],
    easing: 'easeInOutSine',
    duration: 1000,
    loop: true,
    direction: 'alternate'
  });
});
</script>

<style scoped>
  #scroll-down {
    text-align: center;
    margin-top: 100px;
    opacity: 0.5;
  }

  svg {
    display: block;
    margin: 0 auto;
  }
</style>

