<template>
  <header id="header">
    <ul class="menu">
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li><nuxt-link to="/#">About</nuxt-link></li>
      <li><nuxt-link to="/#">Works</nuxt-link></li>
      <li><nuxt-link to="/#">Contact</nuxt-link></li>
    </ul>
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
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 60px;
  z-index: 100;
  .menu {
    display: flex;
    justify-content: center;
    margin-top: 20px;
    margin-right: 10%;
    li {
      margin-left: 100px;
      font-size: 15px;
      font-weight: 900;
      font-family: 'Times New Roman', Times, serif;
      list-style: none;
      a {
        color: #555555;
        text-decoration: none;

        &:hover {
          color: #ff0000;
          border-bottom: 0.5px solid #ff0000;
          transition: 0.5s;
        }
      }
    }
  }
}
</style>
