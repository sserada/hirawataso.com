<template>
  <div class="footer">
    <span>Written by </span>
    <a href="https://github.com/fightingsou">Sou Hirawata</a>
    <span> © 2023. </span>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss" scoped>
.footer {
  font-size: 12px;
  color: #999;
  text-align: right;
  margin-right: 100px;
  margin-bottom: 20px;
  a {
    color: #999;
    text-decoration: none;
    &:hover {
      color: #ff4081;
      transition: 3.0s;
    }
  }
}
</style>

