<template>
  <header id="header">
    <img src="~/assets/img/logo.png" alt="logo">

  </header>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  name: 'Header',
})
</script>

<style lang="scss" scoped>
#header {
  img {
    width: 300px;
  }
}
</style>
