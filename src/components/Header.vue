<template>
  <div class="header">
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/Blog">Blog</router-link>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 70px;
  z-index: 999;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  a {
    color: #A7A7A7;
    text-decoration: none;
    margin: 80px 30px;
    font-size: 18px;

    &:hover {
      color: #666;
      transition: all 0.3s ease;
    }
  }
}
</style>
