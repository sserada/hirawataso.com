<template>
  <section class="index">
    <div class="main">
      <img class="logo" src="~assets/images/logo.svg" alt="logo" />
      <h1 class="border"></h1>
      <div class="scroll-icon">
        <img class="scroll-img" src="~assets/images/arrow.svg" alt="scroll-down" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss" scoped>
.index {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 90vh;
  .logo {
    display: block;
    filter: drop-shadow(0 0 0.25rem #333);
    width: 100%;
    max-width: 500px;
    margin: auto;
    margin-right: 700px;
  }
  .border {
    border-bottom: 0.5px solid #333;
    filter: drop-shadow(0 0 0.25rem #000);
    width: 20%;
    max-width: 500px;
    margin: auto;
    margin-top: 40px;
    margin-right: 700px;
  }
  .scroll-icon {
    position: absolute;
    color: #333;
    bottom: 40px;
    left: 50%;
    font-size: 0.6em;
    animation: bounce 2s infinite;
    .scroll-img {
      width: 30px;
      height: 30px;
      rotate: 90deg;
    }
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
      transform: translateY(0);
    }
    40% {
      transform: translateY(-30px);
    }
    60% {
      transform: translateY(-15px);
    }
  }
}
</style>
