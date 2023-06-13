<template>
  <div class="index">
    <img src="~assets/images/logo.png" />
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style lang="scss" scoped>
.index {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  img {
    width: 100%;
    max-width: 500px;
  }
}
</style>
